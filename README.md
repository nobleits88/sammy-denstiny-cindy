# 蝦米八字命理 — Cindy Plugin

`蝦米八字命理` is a Cindy Plugin for generating and interpreting traditional BaZi (Four Pillars of Destiny) charts. It supports multiple saved profiles, chart calculations, detailed readings, daily fortune schedules, and text or PDF report output.

- **Current version:** `1.1.0`
- **Plugin ID:** `sammy-denstiny`
- **Minimum Cindy version:** `0.1.115`
- **GitHub:** <https://github.com/nobleits88/sammy-denstiny>

> 命理內容只供個人參考及娛樂用途，不構成醫療診斷、投資／財務建議、法律意見、就業保證或其他重大決策保證。

## Features of the Plugin

### Profile and chart management

- Create and save multiple people's BaZi profiles.
- Store name, gender, Gregorian birth date, birth time, and birthplace.
- Select a specific saved profile before viewing a chart or generating a reading.
- Support charts without a birth time; the three available pillars are calculated and the missing hour pillar is clearly identified.
- Keep profile data, chart results, report caches, questions, and schedules isolated within the Plugin.

### BaZi calculations and readings

- Four Pillars and hidden stems.
- Five Elements and strength analysis.
- Ten Gods and chart structure.
- Na Yin.
- Twelve Life Stages.
- Core and supplementary Shen Sha analysis.
- Major Luck Cycles (Da Yun).
- Annual and monthly fortune analysis.
- Custom questions based on the selected chart.

### Reports and daily fortune

- Full text reports in the Cindy conversation.
- Self-contained PDF reports.
- Daily fortune analysis for one explicitly selected profile.
- Recurring daily Schedule Tasks with a configurable time and timezone.
- Comments and donation information, including the bundled Alipay QR code.

## How to Use the Plugin

### 1. Start the Plugin

In Cindy, enter:

```text
八字
```

The Plugin first displays the available profiles and asks you to choose one:

1. Use the current profile.
2. Select another saved profile.
3. Create a new profile.

A chart is not selected automatically. Choose a profile before requesting a reading.

### 2. Create a new profile

When creating a profile, provide:

- Name
- Gender: `男` or `女`
- Gregorian birth date: `YYYY-MM-DD`
- Birth time: `HH:MM` in 24-hour format; leave blank if unknown
- Birthplace

### 3. Choose a function

After selecting a profile, choose one of the following menu items:

1. Chart and chart-structure interpretation
2. Five Elements and Ten Gods details
3. Na Yin and Shen Sha details
4. Major Luck Cycle analysis
5. Annual fortune analysis
6. Ask a custom question
7. Enable or disable daily fortune analysis
8. Comments, donation, and contact information

For menu items 1–5, choose either:

- `1` / `text` — full text report in the conversation
- `2` / `pdf` — PDF report

Menu item 6 accepts a question directly, for example:

```text
我適合從事甚麼工作？
```

### 4. Request today's fortune

If a daily fortune Schedule Task has already been configured, enter:

```text
流日分析
```

The Plugin uses the profile explicitly bound to that schedule. It does not silently switch to another active profile.

### 5. Configure daily fortune analysis

1. Choose menu item `7`.
2. Select exactly one saved profile.
3. Provide a daily report time, such as `09:00`.
4. Provide a timezone, such as `Asia/Hong_Kong`.
5. Cindy creates a recurring Schedule Task for that profile.

A schedule is bound to one profile and does not follow later changes to the global active profile.

## Installation of the Plugin

### Install from a `.cindy` package

1. Download a release package from the GitHub repository or another trusted source:

   ```text
   sammy-denstiny-1.1.0.cindy
   ```

2. Open Cindy's Plugin management interface.
3. Choose **Install** or **Import local Plugin package**.
4. Select the `.cindy` file.
5. Complete the installation and enable the Plugin if prompted.
6. Enter `八字` in Cindy to start using it.

Cindy `0.1.115` or later is required. Do not modify the `.cindy` package or place private profile data, passwords, or tokens inside it.

### Update an existing installation

Keep the Plugin ID unchanged:

```text
sammy-denstiny
```

Import the newer `.cindy` package through Cindy's Plugin management interface. After updating, verify that saved profiles, reports, and Schedule Tasks are still available.

### Development installation

The canonical development source is:

```text
D:\Projects\Cindy\sammy-denstiny
```

Development workflow:

```text
Modify the source in D:\Projects\Cindy\sammy-denstiny
        ↓
Run the project validation and build checks
        ↓
Package with Cindy Forge
        ↓
Install the generated package for testing
        ↓
Commit source changes to SVN
```

The old `cindy-brain` directory is a Cindy Host-managed installation/state directory and must not be used as the development or upgrade source.

## Donation Information

If this Plugin is useful to you and you would like to support continued development, voluntary donations are welcome.

- **Developer email:** <sammy@cpu88.com>
- **Donation method:** Alipay
- **Bundled QR code:** `assets/alipay-donation-qrcode.jpg`

The Plugin's donation menu displays the bundled Alipay QR code and contact information. Donations are voluntary and do not provide additional features, priority support, or guaranteed results.

## Data and Privacy

Each Plugin installation has its own storage scope. The Plugin does not intentionally share profiles with other Plugins such as Zi Wei Dou Shu, I Ching Tarot, or Mei Hua Yi Shu.

Stored data may include:

- Birth information
- Calculated charts
- Profile review status
- Report caches
- Custom questions and answers
- Daily Schedule Task settings

Keep backups of important data before changing installations or devices. Actual data retention and protection depend on Cindy's storage, permissions, and device settings.

## Versioning

Versions use the format:

```text
MajorVersion.MinorVersion.BuildNo
```

The current version is `1.1.0`. The MinorVersion is increased only when the developer explicitly declares a version upgrade. Routine repackaging, testing, or installation updates increase only the BuildNo.

## Disclaimer

BaZi interpretations are provided for personal reference and entertainment only. They are not medical diagnoses, financial or investment advice, legal advice, employment guarantees, or guarantees about future outcomes. Consult qualified professionals for health, financial, legal, relationship, or other important decisions.
