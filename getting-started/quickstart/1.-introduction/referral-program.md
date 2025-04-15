---
icon: calendar-users
---

# Referral Program

The **Referral Program** is a key feature of **TruthWeb** , designed to incentivize users to invite friends and grow the Pi Network ecosystem. By referring new users, participants can earn Pi rewards, bonuses, and other benefits. Below is a detailed breakdown of how the program works, its benefits, implementation details, and use cases.

***

### **Table of Contents**

1. [Overview](referral-program.md#overview-less-than-a-name-overview-greater-than-less-than-a-greater-than)
2. [How It Works](referral-program.md#how-it-works-less-than-a-name-how-it-works-greater-than-less-than-a-greater-than)
3. [Key Benefits](referral-program.md#key-benefits-less-than-a-name-key-benefits-greater-than-less-than-a-greater-than)
4. [Implementation Details](referral-program.md#implementation-details-less-than-a-name-implementation-details-greater-than-less-than-a-greater-than)
5. [Use Cases](referral-program.md#use-cases-less-than-a-name-use-cases-greater-than-less-than-a-greater-than)
6. [FAQs](referral-program.md#faqs-less-than-a-name-faqs-greater-than-less-than-a-greater-than)

***

### **Overview** \<a name="overview">\</a>

The **Referral Program** encourages existing users (referred to as "Pioneers") to invite others to join the Pi Network and TruthWeb platform. For every successful referral, both the referrer and the referred user receive rewards in the form of Pi tokens. This program fosters community growth, increases adoption, and strengthens the Pi ecosystem.

***

### **How It Works** \<a name="how-it-works">\</a>

The **Referral Program** operates through a simple and transparent process:

1. **Generate Referral Link** :
   * Users can generate a unique referral link from their profile or wallet dashboard.
   * Example: `https://truthweb.com/referral/your-username`.
2. **Share the Link** :
   * Share the referral link via social media, email, messaging apps, or other platforms.
   * The link directs new users to the TruthWeb registration page.
3. **New User Joins** :
   * When someone clicks the referral link and signs up, they are tagged as a referral of the original user.
4. **Earn Rewards** :
   * Once the referred user completes specific actions (e.g., verifying their account, making their first transaction), both the referrer and the referred user receive Pi rewards.
5. **Track Progress** :
   * Users can track their referrals, rewards, and bonuses in real-time through the **Referral Dashboard** .

***

### **Key Benefits** \<a name="key-benefits">\</a>

1. **Community Growth** :
   * Encourages organic growth by leveraging word-of-mouth marketing.
2. **Incentivized Participation** :
   * Rewards users for actively contributing to the Pi Network ecosystem.
3. **Increased Adoption** :
   * More users joining the platform leads to greater utility and value for Pi.
4. **Transparency** :
   * All rewards and bonuses are recorded on the blockchain for accountability.
5. **Gamification** :
   * Leaderboards and milestones motivate users to refer more people.

***

### **Implementation Details** \<a name="implementation-details">\</a>

#### **Core Components**

1. **Smart Contracts** :
   * Automate reward distribution based on predefined rules.
   * Example: A smart contract releases Pi tokens to both the referrer and the referred user after verification.

// Solidity Smart Contract for Referral Rewards pragma solidity ^0.8.0;

contract ReferralProgram { mapping(address => address) public referrals; mapping(address => uint256) public rewards;

```
event ReferralReward(address indexed referrer, address indexed referred, uint256 amount);

function addReferral(address referrer, address referred) external {
    require(referrals[referred] == address(0), "User already referred");
    referrals[referred] = referrer;
}

function distributeRewards(address referred, uint256 rewardAmount) external {
    address referrer = referrals[referred];
    require(referrer != address(0), "No referrer found");

    rewards[referrer] += rewardAmount;
    rewards[referred] += rewardAmount;

    emit ReferralReward(referrer, referred, rewardAmount);
}

}
```

1. **Referral Dashboard** :
   * Provides a user-friendly interface to track referrals, rewards, and progress.
   * Example Metrics:
     * Total Referrals
     * Pending Rewards
     * Claimed Rewards
2. **API Integration** :
   * APIs connect the frontend (referral system) with the backend (reward distribution).
   * Example: An API endpoint to fetch referral statistics.

```javascript
app.get('/api/referrals/:userId', async (req, res) => {
    const userId = req.params.userId;
    const referralData = await fetchReferralData(userId);
    res.json(referralData);
});
```

1. **Blockchain Tracking** :
   * All referral activities and rewards are recorded on the Pi Network blockchain for transparency.

***

### **Use Cases** \<a name="use-cases">\</a>

1. **Earning Passive Income** :
   * Users can earn Pi rewards by simply inviting friends and family.
2. **Building Teams** :
   * Entrepreneurs and community leaders can build referral teams to maximize earnings.
3. **Promoting Digital Goods** :
   * Vendors can use the referral program to promote their marketplace listings.
4. **Cross-Promotion** :
   * Partner with other Pi Network users to cross-promote each other’s referral links.
5. **Community Engagement** :
   * Host contests or challenges to encourage referrals and boost engagement.

***

### **FAQs** \<a name="faqs">\</a>

#### Q: How do I join the Referral Program?

A: Simply sign up on TruthWeb and generate your unique referral link from the Referral Dashboard.

#### Q: How much Pi can I earn per referral?

A: The reward amount varies based on the user's activity and the platform's policies. Typically, both the referrer and the referred user receive a fixed amount of Pi.

#### Q: Can I refer unlimited users?

A: Yes, there is no limit to the number of referrals you can make.

#### Q: How are rewards distributed?

A: Rewards are distributed automatically via smart contracts once the referred user completes the required actions.

#### Q: Where can I track my referrals and rewards?

A: You can view your referrals, rewards, and progress in the **Referral Dashboard** under your profile.

***

For further inquiries or technical support, visit the[ Support Center .](../support.md)
