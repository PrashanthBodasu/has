/**
 * Project: Herbal Facial Scrub Formulation & Development
 * Description: Simulates the step-by-step compounding and preparation process.
 */

class HerbalPreparationProcess {
    constructor(productName, totalBatchGrams) {
        this.productName = productName;
        this.totalBatchGrams = totalBatchGrams;
        this.isComplete = false;
    }

    // Define the exact formulation ingredients and weights
    getFormulation() {
        return {
            "Phase A (Aqueous)": "Distilled Water, Glycerin, Xanthan Gum",
            "Phase B (Lipid/Oil)": "Almond Oil, Cetyl Alcohol, Emulsifying Wax",
            "Phase C (Herbal Actives & Exfoliants)": "Neem Extract, Aloe Vera Gel, Walnut Shell Powder",
            "Phase D (Preservative)": "Phenoxyethanol"
        };
    }

    // Execute the step-by-step manufacturing process
    runManufacturingSteps() {
        console.log(`========================================`);
        console.log(`Starting Batch: ${this.productName}`);
        console.log(`Total Target Weight: ${this.totalBatchGrams}g`);
        console.log(`========================================\n`);

        console.log("1. Dispensing & Weighing:");
        console.log("   -> Accurately weigh all raw materials according to formula percentages.\n");

        console.log("2. Phase Preparation:");
        console.log("   -> Heat Phase A and Phase B separately to 75°C - 80°C.");
        console.log("   -> Dissolve water-soluble gums and mix oil components thoroughly.\n");

        console.log("3. Emulsification & Blending:");
        console.log("   -> Slowly pour Phase B into Phase A under continuous mechanical stirring.");
        console.log("   -> Homogenize until a uniform cream base is formed.\n");

        console.log("4. Incorporation of Herbal Actives (Phase C):");
        console.log("   -> Allow the base to cool below 40°C.");
        console.log("   -> Gently fold in Neem extract, Aloe vera, and Walnut shell powder to prevent thermal degradation of actives.\n");

        console.log("5. Quality Control (QC):");
        console.log("   -> Check physical appearance, texture, and verify pH is between 5.5 - 6.5.");
        
        this.isComplete = true;
        console.log("\n[SUCCESS]: Herbal Facial Scrub preparation process completed successfully!");
    }
}

// Run the preparation process
const myScrubBatch = new HerbalPreparationProcess("Herbal Facial Scrub", 100);
const formulationTable = myScrubBatch.getFormulation();

console.log("Formulation Ingredients:", formulationTable);
myScrubBatch.runManufacturingSteps();
