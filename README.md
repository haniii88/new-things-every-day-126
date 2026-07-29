/* New Things Every Day — Day 126 */
/* Analyzes cod review activity and creates a development summary */

function dailyLog126() {
    const reviews = [
        { reviewer: "Alex", approved: true },
        { reviewer: "Maria", approved: true },
        { reviewer: "John", approved: false },
        { reviewer: "Sara", approved: true }
    ];

    const approvedReviews = reviews.filter(
        review => review.approved
    ).length;

    const report = {
        day: 126,
        timestamp: new Date().toISOString(),
        totalReviews: reviews.length,
        approved: approvedReviews,
        rejected: reviews.length - approvedReviews,
        approvalRate: `${Math.round(
            (approvedReviews / reviews.length) * 100
        )}%`
    };

    console.log("Day 126 Code Review Report:", report);
}

dailyLog126();
