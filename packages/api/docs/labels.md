<!-- this doc is generated by ./scripts/docs/labels.mjs -->

  # Labels
  
  This document is a reference for the labels used in the SDK.

  **⚠️ Note**: These labels are still in development and may change over time. Not all are currently in use.

  ## Key

  ### Label Preferences

  The possible client interpretations for a label.

  - <code>ignore</code> Do nothing with the label.
  - <code>warn</code> Provide some form of warning on the content (see "On Warn" behavior).
  - <code>hide</code> Remove the content from feeds and apply the warning when directly viewed.

  Each label specifies which preferences it can support. If a label is not configurable, it must have only own supported preference.

  ### Configurable?

  Non-configurable labels cannot have their preference changed by the user.

  ### Flags

  Additional behaviors which a label can adopt.

  - <code>no-override</code> The user cannot click through any covering of content created by the label.
  - <code>adult</code> The user must have adult content enabled to configure the label. If adult content is not enabled, the label must adopt the strictest preference.

  ### On Warn

  The kind of UI behavior used when a warning must be applied.

  - <code>blur</code> Hide all of the content behind an interstitial.
  - <code>blur-media</code> Hide only the media within the content (ie images) behind an interstitial.
  - <code>alert</code> Display a descriptive warning but do not hide the content.
  - <code>null</code> Do nothing.

  ## Label Behaviors

  <table>
    <tr>
      <th>ID</th>
      <th>Group</th>
      <th>Preferences</th>
      <th>Configurable</th>
      <th>Flags</th>
      <th>On Warn</th>
    </tr>
    <tr>
  <td>!hide</td>
  <td>system</td>
  <td>hide</td>
  <td>❌</td>
  <td>no-override</td>
  <td>blur</td>
</tr>
<tr>
  <td>!no-promote</td>
  <td>system</td>
  <td>hide</td>
  <td>❌</td>
  <td></td>
  <td>null</td>
</tr>
<tr>
  <td>!warn</td>
  <td>system</td>
  <td>warn</td>
  <td>❌</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>dmca-violation</td>
  <td>legal</td>
  <td>hide</td>
  <td>❌</td>
  <td>no-override</td>
  <td>blur</td>
</tr>
<tr>
  <td>doxxing</td>
  <td>legal</td>
  <td>hide</td>
  <td>❌</td>
  <td>no-override</td>
  <td>blur</td>
</tr>
<tr>
  <td>porn</td>
  <td>sexual</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td>adult</td>
  <td>blur-media</td>
</tr>
<tr>
  <td>sexual</td>
  <td>sexual</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td>adult</td>
  <td>blur-media</td>
</tr>
<tr>
  <td>nudity</td>
  <td>sexual</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td>adult</td>
  <td>blur-media</td>
</tr>
<tr>
  <td>nsfl</td>
  <td>violence</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td>adult</td>
  <td>blur-media</td>
</tr>
<tr>
  <td>corpse</td>
  <td>violence</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td>adult</td>
  <td>blur-media</td>
</tr>
<tr>
  <td>gore</td>
  <td>violence</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td>adult</td>
  <td>blur-media</td>
</tr>
<tr>
  <td>torture</td>
  <td>violence</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td>adult</td>
  <td>blur</td>
</tr>
<tr>
  <td>self-harm</td>
  <td>violence</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td>adult</td>
  <td>blur-media</td>
</tr>
<tr>
  <td>intolerant-race</td>
  <td>intolerance</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>intolerant-gender</td>
  <td>intolerance</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>intolerant-sexual-orientation</td>
  <td>intolerance</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>intolerant-religion</td>
  <td>intolerance</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>intolerant</td>
  <td>intolerance</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>icon-intolerant</td>
  <td>intolerance</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur-media</td>
</tr>
<tr>
  <td>threat</td>
  <td>rude</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>spoiler</td>
  <td>curation</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>spam</td>
  <td>spam</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>account-security</td>
  <td>misinfo</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>net-abuse</td>
  <td>misinfo</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>blur</td>
</tr>
<tr>
  <td>impersonation</td>
  <td>misinfo</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>alert</td>
</tr>
<tr>
  <td>scam</td>
  <td>misinfo</td>
  <td>ignore, warn, hide</td>
  <td>✅</td>
  <td></td>
  <td>alert</td>
</tr>
  </table>

  ## Label Group Descriptions

  <table>
    <tr>
      <th>ID</th>
      <th>Description</th>
    </tr>
    <tr>
  <td>system</td>
  <td><code>general</code><br><strong>System</strong><br>Moderator overrides for special cases.</td>
</tr>
<tr>
  <td>legal</td>
  <td><code>general</code><br><strong>Legal</strong><br>Content removed for legal reasons.</td>
</tr>
<tr>
  <td>sexual</td>
  <td><code>general</code><br><strong>Adult Content</strong><br>Content which is sexual in nature.</td>
</tr>
<tr>
  <td>violence</td>
  <td><code>general</code><br><strong>Violence</strong><br>Content which is violent or deeply disturbing.</td>
</tr>
<tr>
  <td>intolerance</td>
  <td><code>general</code><br><strong>Intolerance</strong><br>Content or behavior which is hateful or intolerant toward a group of people.</td>
</tr>
<tr>
  <td>rude</td>
  <td><code>general</code><br><strong>Rude</strong><br>Behavior which is rude toward other users.</td>
</tr>
<tr>
  <td>curation</td>
  <td><code>general</code><br><strong>Curational</strong><br>Subjective moderation geared towards curating a more positive environment.</td>
</tr>
<tr>
  <td>spam</td>
  <td><code>general</code><br><strong>Spam</strong><br>Content which doesn't add to the conversation.</td>
</tr>
<tr>
  <td>misinfo</td>
  <td><code>general</code><br><strong>Misinformation</strong><br>Content which misleads or defrauds users.</td>
</tr>
  </table>

  ## Label Descriptions

  <table>
    <tr>
      <th>ID</th>
      <th>Description</th>
    </tr>
    <tr>
  <td>!hide</td>
  <td>
    <code>general</code><br><strong>Moderator Hide</strong><br>Moderator has chosen to hide the content.<br><br>
    <code>on an account</code><br><strong>Content Blocked</strong><br>This account has been hidden by the moderators.<br><br>
    <code>on content</code><br><strong>Content Blocked</strong><br>This content has been hidden by the moderators.<br><br>
  </td>
</tr>
<tr>
  <td>!no-promote</td>
  <td>
    <code>general</code><br><strong>Moderator Filter</strong><br>Moderator has chosen to filter the content from feeds.<br><br>
    <code>on an account</code><br><strong>N/A</strong><br>N/A<br><br>
    <code>on content</code><br><strong>N/A</strong><br>N/A<br><br>
  </td>
</tr>
<tr>
  <td>!warn</td>
  <td>
    <code>general</code><br><strong>Moderator Warn</strong><br>Moderator has chosen to set a general warning on the content.<br><br>
    <code>on an account</code><br><strong>Content Warning</strong><br>This account has received a general warning from moderators.<br><br>
    <code>on content</code><br><strong>Content Warning</strong><br>This content has received a general warning from moderators.<br><br>
  </td>
</tr>
<tr>
  <td>dmca-violation</td>
  <td>
    <code>general</code><br><strong>Copyright Violation</strong><br>The content has received a DMCA takedown request.<br><br>
    <code>on an account</code><br><strong>Copyright Violation</strong><br>This account has received a DMCA takedown request. It will be restored if the concerns can be resolved.<br><br>
    <code>on content</code><br><strong>Copyright Violation</strong><br>This content has received a DMCA takedown request. It will be restored if the concerns can be resolved.<br><br>
  </td>
</tr>
<tr>
  <td>doxxing</td>
  <td>
    <code>general</code><br><strong>Doxxing</strong><br>Information that reveals private information about someone which has been shared without the consent of the subject.<br><br>
    <code>on an account</code><br><strong>Doxxing</strong><br>This account has been reported to publish private information about someone without their consent. This report is currently under review.<br><br>
    <code>on content</code><br><strong>Doxxing</strong><br>This content has been reported to include private information about someone without their consent.<br><br>
  </td>
</tr>
<tr>
  <td>porn</td>
  <td>
    <code>general</code><br><strong>Pornography</strong><br>Images of full-frontal nudity (genitalia) in any sexualized context, or explicit sexual activity (meaning contact with genitalia or breasts) even if partially covered. Includes graphic sexual cartoons (often jokes/memes).<br><br>
    <code>on an account</code><br><strong>Adult Content</strong><br>This account contains imagery of full-frontal nudity or explicit sexual activity.<br><br>
    <code>on content</code><br><strong>Adult Content</strong><br>This content contains imagery of full-frontal nudity or explicit sexual activity.<br><br>
  </td>
</tr>
<tr>
  <td>sexual</td>
  <td>
    <code>general</code><br><strong>Sexually Suggestive</strong><br>Content that does not meet the level of "pornography", but is still sexual. Some common examples have been selfies and "hornyposting" with underwear on, or partially naked (naked but covered, eg with hands or from side perspective). Sheer/see-through nipples may end up in this category.<br><br>
    <code>on an account</code><br><strong>Suggestive Content</strong><br>This account contains imagery which is sexually suggestive. Common examples include selfies in underwear or in partial undress.<br><br>
    <code>on content</code><br><strong>Suggestive Content</strong><br>This content contains imagery which is sexually suggestive. Common examples include selfies in underwear or in partial undress.<br><br>
  </td>
</tr>
<tr>
  <td>nudity</td>
  <td>
    <code>general</code><br><strong>Nudity</strong><br>Nudity which is not sexual, or that is primarily "artistic" in nature. For example: breastfeeding; classic art paintings and sculptures; newspaper images with some nudity; fashion modeling. "Erotic photography" is likely to end up in sexual or porn.<br><br>
    <code>on an account</code><br><strong>Adult Content</strong><br>This account contains imagery which portrays nudity in a non-sexual or artistic setting.<br><br>
    <code>on content</code><br><strong>Adult Content</strong><br>This content contains imagery which portrays nudity in a non-sexual or artistic setting.<br><br>
  </td>
</tr>
<tr>
  <td>nsfl</td>
  <td>
    <code>general</code><br><strong>NSFL</strong><br>"Not Suitable For Life." This includes graphic images like the infamous "goatse" (don't look it up).<br><br>
    <code>on an account</code><br><strong>Graphic Imagery (NSFL)</strong><br>This account contains graphic images which are often referred to as "Not Suitable For Life."<br><br>
    <code>on content</code><br><strong>Graphic Imagery (NSFL)</strong><br>This content contains graphic images which are often referred to as "Not Suitable For Life."<br><br>
  </td>
</tr>
<tr>
  <td>corpse</td>
  <td>
    <code>general</code><br><strong>Corpse</strong><br>Visual image of a dead human body in any context. Includes war images, hanging, funeral caskets. Does not include all figurative cases (cartoons), but can include realistic figurative images or renderings.<br><br>
    <code>on an account</code><br><strong>Graphic Imagery (Corpse)</strong><br>This account contains images of a dead human body in any context. Includes war images, hanging, funeral caskets.<br><br>
    <code>on content</code><br><strong>Graphic Imagery (Corpse)</strong><br>This content contains images of a dead human body in any context. Includes war images, hanging, funeral caskets.<br><br>
  </td>
</tr>
<tr>
  <td>gore</td>
  <td>
    <code>general</code><br><strong>Gore</strong><br>Intended for shocking images, typically involving blood or visible wounds.<br><br>
    <code>on an account</code><br><strong>Graphic Imagery (Gore)</strong><br>This account contains shocking images involving blood or visible wounds.<br><br>
    <code>on content</code><br><strong>Graphic Imagery (Gore)</strong><br>This content contains shocking images involving blood or visible wounds.<br><br>
  </td>
</tr>
<tr>
  <td>torture</td>
  <td>
    <code>general</code><br><strong>Torture</strong><br>Depictions of torture of a human or animal (animal cruelty).<br><br>
    <code>on an account</code><br><strong>Graphic Imagery (Torture)</strong><br>This account contains depictions of torture of a human or animal.<br><br>
    <code>on content</code><br><strong>Graphic Imagery (Torture)</strong><br>This content contains depictions of torture of a human or animal.<br><br>
  </td>
</tr>
<tr>
  <td>self-harm</td>
  <td>
    <code>general</code><br><strong>Self-Harm</strong><br>A visual depiction (photo or figurative) of cutting, suicide, or similar.<br><br>
    <code>on an account</code><br><strong>Graphic Imagery (Self-Harm)</strong><br>This account includes depictions of cutting, suicide, or other forms of self-harm.<br><br>
    <code>on content</code><br><strong>Graphic Imagery (Self-Harm)</strong><br>This content includes depictions of cutting, suicide, or other forms of self-harm.<br><br>
  </td>
</tr>
<tr>
  <td>intolerant-race</td>
  <td>
    <code>general</code><br><strong>Racial Intolerance</strong><br>Hateful or intolerant content related to race.<br><br>
    <code>on an account</code><br><strong>Intolerance (Racial)</strong><br>This account includes hateful or intolerant content related to race.<br><br>
    <code>on content</code><br><strong>Intolerance (Racial)</strong><br>This content includes hateful or intolerant views related to race.<br><br>
  </td>
</tr>
<tr>
  <td>intolerant-gender</td>
  <td>
    <code>general</code><br><strong>Gender Intolerance</strong><br>Hateful or intolerant content related to gender or gender identity.<br><br>
    <code>on an account</code><br><strong>Intolerance (Gender)</strong><br>This account includes hateful or intolerant content related to gender or gender identity.<br><br>
    <code>on content</code><br><strong>Intolerance (Gender)</strong><br>This content includes hateful or intolerant views related to gender or gender identity.<br><br>
  </td>
</tr>
<tr>
  <td>intolerant-sexual-orientation</td>
  <td>
    <code>general</code><br><strong>Sexual Orientation Intolerance</strong><br>Hateful or intolerant content related to sexual preferences.<br><br>
    <code>on an account</code><br><strong>Intolerance (Orientation)</strong><br>This account includes hateful or intolerant content related to sexual preferences.<br><br>
    <code>on content</code><br><strong>Intolerance (Orientation)</strong><br>This content includes hateful or intolerant views related to sexual preferences.<br><br>
  </td>
</tr>
<tr>
  <td>intolerant-religion</td>
  <td>
    <code>general</code><br><strong>Religious Intolerance</strong><br>Hateful or intolerant content related to religious views or practices.<br><br>
    <code>on an account</code><br><strong>Intolerance (Religious)</strong><br>This account includes hateful or intolerant content related to religious views or practices.<br><br>
    <code>on content</code><br><strong>Intolerance (Religious)</strong><br>This content includes hateful or intolerant views related to religious views or practices.<br><br>
  </td>
</tr>
<tr>
  <td>intolerant</td>
  <td>
    <code>general</code><br><strong>Intolerance</strong><br>A catchall for hateful or intolerant content which is not covered elsewhere.<br><br>
    <code>on an account</code><br><strong>Intolerance</strong><br>This account includes hateful or intolerant content.<br><br>
    <code>on content</code><br><strong>Intolerance</strong><br>This content includes hateful or intolerant views.<br><br>
  </td>
</tr>
<tr>
  <td>icon-intolerant</td>
  <td>
    <code>general</code><br><strong>Intolerant Iconography</strong><br>Visual imagery associated with a hate group, such as the KKK or Nazi, in any context (supportive, critical, documentary, etc).<br><br>
    <code>on an account</code><br><strong>Intolerant Iconography</strong><br>This account includes imagery associated with a hate group such as the KKK or Nazis. This warning may apply to content any context, including critical or documentary purposes.<br><br>
    <code>on content</code><br><strong>Intolerant Iconography</strong><br>This content includes imagery associated with a hate group such as the KKK or Nazis. This warning may apply to content any context, including critical or documentary purposes.<br><br>
  </td>
</tr>
<tr>
  <td>threat</td>
  <td>
    <code>general</code><br><strong>Threats</strong><br>Statements or imagery published with the intent to threaten, intimidate, or harm.<br><br>
    <code>on an account</code><br><strong>Threats</strong><br>The moderators believe this account has published statements or imagery with the intent to threaten, intimidate, or harm others.<br><br>
    <code>on content</code><br><strong>Threats</strong><br>The moderators believe this content was published with the intent to threaten, intimidate, or harm others.<br><br>
  </td>
</tr>
<tr>
  <td>spoiler</td>
  <td>
    <code>general</code><br><strong>Spoiler</strong><br>Discussion about film, TV, etc which gives away plot points.<br><br>
    <code>on an account</code><br><strong>Spoiler Warning</strong><br>This account contains discussion about film, TV, etc which gives away plot points.<br><br>
    <code>on content</code><br><strong>Spoiler Warning</strong><br>This content contains discussion about film, TV, etc which gives away plot points.<br><br>
  </td>
</tr>
<tr>
  <td>spam</td>
  <td>
    <code>general</code><br><strong>Spam</strong><br>Repeat, low-quality messages which are clearly not designed to add to a conversation or space.<br><br>
    <code>on an account</code><br><strong>Spam</strong><br>This account publishes repeat, low-quality messages which are clearly not designed to add to a conversation or space.<br><br>
    <code>on content</code><br><strong>Spam</strong><br>This content is a part of repeat, low-quality messages which are clearly not designed to add to a conversation or space.<br><br>
  </td>
</tr>
<tr>
  <td>account-security</td>
  <td>
    <code>general</code><br><strong>Security Concerns</strong><br>Content designed to hijack user accounts such as a phishing attack.<br><br>
    <code>on an account</code><br><strong>Security Warning</strong><br>This account has published content designed to hijack user accounts such as a phishing attack.<br><br>
    <code>on content</code><br><strong>Security Warning</strong><br>This content is designed to hijack user accounts such as a phishing attack.<br><br>
  </td>
</tr>
<tr>
  <td>net-abuse</td>
  <td>
    <code>general</code><br><strong>Network Attacks</strong><br>Content designed to attack network systems such as denial-of-service attacks.<br><br>
    <code>on an account</code><br><strong>Network Attack Warning</strong><br>This account has published content designed to attack network systems such as denial-of-service attacks.<br><br>
    <code>on content</code><br><strong>Network Attack Warning</strong><br>This content is designed to attack network systems such as denial-of-service attacks.<br><br>
  </td>
</tr>
<tr>
  <td>impersonation</td>
  <td>
    <code>general</code><br><strong>Impersonation</strong><br>Accounts which falsely assert some identity.<br><br>
    <code>on an account</code><br><strong>Impersonation Warning</strong><br>The moderators believe this account is lying about their identity.<br><br>
    <code>on content</code><br><strong>Impersonation Warning</strong><br>The moderators believe this account is lying about their identity.<br><br>
  </td>
</tr>
<tr>
  <td>scam</td>
  <td>
    <code>general</code><br><strong>Scam</strong><br>Fraudulent content.<br><br>
    <code>on an account</code><br><strong>Scam Warning</strong><br>The moderators believe this account publishes fraudulent content.<br><br>
    <code>on content</code><br><strong>Scam Warning</strong><br>The moderators believe this is fraudulent content.<br><br>
  </td>
</tr>
  </table>