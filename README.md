# SuperTag

A flexible tag component for Budibase applications that supports text labels, icons, customizable styling, and optional hideable functionality for status indicators, categories, and annotations.

## 🚀 Features

### Tag Display Options

- **Text Content**: Custom text labels with template support
- **Icon Integration**: Optional icons for visual context
- **Size Variants**: Small, medium, and large sizing options
- **Color Customization**: Background and text color control

### Interactive Features

- **Hideable Functionality**: Optional user-dismissible tags
- **Event Handling**: Trigger actions when tags are hidden
- **Template Support**: Dynamic content based on data
- **Flexible Positioning**: Independent component placement

### Styling Control

- **Color Theming**: Custom background and text colors
- **Typography**: Consistent font sizing across sizes
- **Visual Consistency**: Integration with Budibase design system
- **Responsive Design**: Adapts to different screen sizes

## 🎯 Usage Instructions

### Basic Setup

1. Add the SuperTag component to your screen
2. Configure the text content (static or dynamic)
3. Choose size and color customization
4. Optionally enable hideable functionality
5. Position appropriately in your layout

### Content Configuration

- **Text Field**: Static text or template binding for dynamic content
- **Icon Selection**: Choose from available icon library
- **Size Options**: Small for compact space, medium for standard use, large for emphasis
- **Color Coordination**: Match tag colors with application theme

### Hideable Functionality

- **User Interaction**: Allow users to dismiss tags
- **Event Triggering**: Fire onHide events for action coordination
- **State Management**: Track which tags have been hidden
- **Persistent Actions**: Maintain hide state across sessions

## 🔧 Configuration Properties

### Core Tag Settings

- **Text**: Tag text content (supports template bindings)
- **Icon**: Optional icon for visual context
- **Size**: Small, Medium, or Large sizing
- **Color**: Background color customization
- **Text Color**: Text color customization

### Interactive Settings

- **Hideable**: Enable/disable user dismissal capability
- **On Hide**: Event triggered when tag is hidden by user

## 📋 Usage Examples

### Status Indicator Tag

Create status indicators with consistent color coding:

- Text: `{{ status }}`
- Color: Dynamic based on status (green for success, red for error)
- Size: Small
- Icon: Status-appropriate icons

### Category Tag

Display item categories with visual distinction:

- Text: `{{ category }}`
- Color: Unique colors per category
- Size: Medium
- Icon: Category-specific icons

### User Roles Badge

Show user permissions or roles:

- Text: `{{ user.role }}`
- Color: Role-based color schemes
- Size: Small
- Icon: Person or user-related icons

### Dismissible Notification Tags

Allow users to dismiss notification badges:

- Text: `{{ notification.message }}`
- Color: Attention-grabbing colors
- Size: Medium
- Hideable: Enabled
- On Hide: Update notification status

### Information Labels

Provide contextual information with clear visual cues:

- Text: `{{ info.level }}`
- Color: Appropriate information colors
- Size: Large
- Icon: Information or warning icons

## 🎨 Styling & Theming

### Color Customization

- **Background Color**: Complete color control for tag background
- **Text Color**: Independent text color customization
- **Contrast Management**: Automatic readability optimization
- **Theme Integration**: Consistent with Budibase color system

### Size Variants

- **Small**: Compact tags for minimal space usage
- **Medium**: Standard tags for most common use cases
- **Large**: Emphasized tags for important categories

### Visual States

- **Default State**: Standard appearance with configured colors
- **Hover State**: Subtle visual feedback on interaction
- **Focus State**: Accessible focus indicators for keyboard navigation
- **Hidden State**: Seamless removal when hideable tags are dismissed

## 🔗 Integration

### Data Binding

- **Template Support**: Bind to dynamic data sources
- **Collection Tags**: Work with arrays of tags
- **Conditional Display**: Show/hide tags based on data conditions
- **Dynamic Styling**: Colors and content based on data values

### Component Interaction

- **Parent Communication**: Integration with parent component logic
- **Global State**: Connection to application-wide state management
- **Event Propagation**: Handle tag events in parent components
- **Context Sharing**: Access to application-level data and preferences

### Application Integration

- **Navigation Context**: Tags that link to different application sections
- **Action Triggers**: Tags that initiate specific actions or workflows
- **Filter Integration**: Tags that control data filtering and display
- **User Preferences**: Tags that reflect and modify user settings

## 📱 Responsiveness & Accessibility

### Responsive Behavior

- **Flexible Sizing**: Automatic adaptation to container constraints
- **Content Responsiveness**: Text and icon adjustments for small screens
- **Layout Flexibility**: Works in various layout scenarios
- **Touch-Friendly**: Appropriate size for mobile interactions

### Accessibility Features

- **Sematic Markup**: Proper tag structure for screen readers
- **Color Contrast**: Automatic contrast ratio enforcement
- **Keyboard Navigation**: Full keyboard accessibility support
- **Screen Reader Support**: Descriptive content for assistive technologies

## 🐛 Troubleshooting

### Display Issues

- **Color Visibility**: Ensure sufficient contrast between background and text colors
- **Template Binding**: Verify correct template syntax for dynamic content
- **Icon Rendering**: Check icon availability and naming conventions
- **Size Constraints**: Ensure adequate space for chosen size variant

### Interactive Problems

- **Hide Functionality**: Verify hideable property and event configuration
- **Event Handling**: Check event binding and handler implementation
- **State Management**: Ensure proper tracking of hidden tag state
- **Performance**: Monitor for excessive event triggering in large lists

### Styling Conflicts

- **CSS Overrides**: Check for application-level CSS that may affect tag styling
- **Theme Consistency**: Verify tag colors align with overall application theme
- **Inheritance Issues**: Resolve conflicts with parent component styling
- **Browser Compatibility**: Test styling across different browsers and versions

### Data Integration Challenges

- **Binding Errors**: Validate template binding syntax and data availability
- **Update Timing**: Ensure data updates propagate correctly to tag display
- **Context Access**: Verify access to required data and context variables
- **Performance**: Monitor for performance issues with frequently updating data

Find out more about developing [Custom Plugins](https://docs.budibase.com/docs/custom-plugin) and [Budibase](https://github.com/Budibase/budibase).
