<template>
  <ExampleContainer title="Structure">
    <ExampleContent :code="example1">
      <PPage
        title="Invoice"
        subtitle="Statement period: May 3, 2019 to June 2, 2019">
        <p>Page content</p>
      </PPage>
    </ExampleContent>

    <ExampleContent :code="example2">
      <PLayout>
        <PLayoutAnnotatedSection
          title="Store details"
          description="Shopify and your customers will use this information to contact you.">
          <PCard sectioned>
            <PFormLayout>
              <PTextField label="Store name"/>
              <PTextField type="email" label="Account email"/>
            </PFormLayout>
          </PCard>
        </PLayoutAnnotatedSection>
      </PLayout>
    </ExampleContent>

    <ExampleContent :code="example3">
      <PLayout>
        <PLayoutSection>
          <PCard title="Order details" sectioned>
            <p>View a summary of your order.</p>
          </PCard>
        </PLayoutSection>
        <PLayoutSection secondary>
          <PCard title="Tags" sectioned>
            <p>Add tags to your order.</p>
          </PCard>
        </PLayoutSection>
      </PLayout>
    </ExampleContent>

    <ExampleContent :code="example4">
      <PLayout>
        <PLayoutSection>
          <PCard title="Online store dashboard" sectioned>
            <p>View a summary of your online store’s performance.</p>
          </PCard>
        </PLayoutSection>
      </PLayout>
    </ExampleContent>

    <ExampleContent :code="example5">
      <PStack>
        <PBadge>Paid</PBadge>
        <PBadge>Processing</PBadge>
        <PBadge>Fulfilled</PBadge>
        <PBadge>Completed</PBadge>
      </PStack>
    </ExampleContent>

    <ExampleContent :code="example6">
      <PStack>
        <PStackItem fill>
          <PHeading>Order #1136</PHeading>
        </PStackItem>
        <PStackItem>
          <PBadge>Paid</PBadge>
        </PStackItem>
        <PStackItem>
          <PBadge>Fulfilled</PBadge>
        </PStackItem>
      </PStack>
    </ExampleContent>

    <ExampleContent :code="example7">
      <PCard title="Online store dashboard">
        <PCardSection title="Reports">
          <p>View a summary of your online store’s performance.</p>
        </PCardSection>

        <PCardSection title="Summary">
          <p>
            View a summary of your online store’s performance, including sales,
            visitors, top products, and referrals.
          </p>
        </PCardSection>
      </PCard>

    </ExampleContent>
  </ExampleContainer>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

import { ExampleContainer, ExampleContent } from '@/examples/components';
import { PPage } from '@/components/PPage';
import { PLayout, PLayoutAnnotatedSection, PLayoutSection } from '@/components/PLayout';
import { PCard, PCardSection } from '@/components/PCard';
import { PStack, PStackItem } from '@/components/PStack';
import { PFormLayout } from '@/components/PFormLayout';
import { PHeading } from '@/components/PHeading';
import { PTextField } from '@/components/PTextField';
import { PBadge } from '@/components/PBadge';

@Component({
  components: {
    ExampleContainer, ExampleContent,
    PPage, PLayout, PLayoutAnnotatedSection, PLayoutSection, PCard, PCardSection,
    PStack, PStackItem,
    PFormLayout,
    PHeading,
    PTextField,
    PBadge,
  },
})
export default class StructureExample extends Vue {
  public example1 = `
  <PPage
    title="Invoice"
    subtitle="Statement period: May 3, 2019 to June 2, 2019">
    <p>Page content</p>
  </PPage>
  `;

  public example2 = `
  <PLayout>
    <PLayoutAnnotatedSection
      title="Store details"
      description="Shopify and your customers will use this information to contact you.">
      <PCard sectioned>
        <PFormLayout>
          <PTextField label="Store name"/>
          <PTextField type="email" label="Account email"/>
        </PFormLayout>
      </PCard>
    </PLayoutAnnotatedSection>
  </PLayout>
  `;

  public example3 = `
  <PLayout>
    <PLayoutSection>
      <PCard title="Order details" sectioned>
        <p>View a summary of your order.</p>
      </PCard>
    </PLayoutSection>
    <PLayoutSection secondary>
      <PCard title="Tags" sectioned>
        <p>Add tags to your order.</p>
      </PCard>
    </PLayoutSection>
  </PLayout>
  `;

  public example4 = `
  <PLayout>
    <PLayoutSection>
      <PCard title="Online store dashboard" sectioned>
        <p>View a summary of your online store’s performance.</p>
      </PCard>
    </PLayoutSection>
  </PLayout>
  `;

  public example5 = `
  <PStack>
    <PBadge>Paid</PBadge>
    <PBadge>Processing</PBadge>
    <PBadge>Fulfilled</PBadge>
    <PBadge>Completed</PBadge>
  </PStack>
  `;

  public example6 = `
  <PStack>
    <PStackItem fill>
      <PHeading>Order #1136</PHeading>
    </PStackItem>
    <PStackItem>
      <PBadge>Paid</PBadge>
    </PStackItem>
    <PStackItem>
      <PBadge>Fulfilled</PBadge>
    </PStackItem>
  </PStack>
  `;

  public example7 = `
  <PCard title="Online store dashboard">
    <PCardSection title="Reports">
      <p>View a summary of your online store’s performance.</p>
    </PCardSection>

    <PCardSection title="Summary">
      <p>
        View a summary of your online store’s performance, including sales,
        visitors, top products, and referrals.
      </p>
    </PCardSection>
  </PCard>
  `;
}
</script>
