---
description: Est un entier lié à une propriété avec les qualificateurs BitMap et BitValue.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Qualificateurs BitMap et BitValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536357"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a><span data-ttu-id="02b15-103">Qualificateurs BitMap et BitValue</span><span class="sxs-lookup"><span data-stu-id="02b15-103">BitMap and BitValue Qualifiers</span></span>

<span data-ttu-id="02b15-104">Une image bitmap est un entier lié à une propriété avec les qualificateurs **bitmap** et **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="02b15-104">A bitmap is an integer linked to a property with the **BitMap** and **BitValue** qualifiers.</span></span> <span data-ttu-id="02b15-105">Chaque bit de la valeur de propriété agit comme un index dans le tableau de valeurs de la liste **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="02b15-105">Each bit of the property value acts as an index into the array of values in the **BitValue** list.</span></span> <span data-ttu-id="02b15-106">Étant donné que plusieurs bits de la valeur de propriété peuvent être « on » en même temps, il est possible d’utiliser une seule valeur de propriété pour indiquer plusieurs valeurs simultanées.</span><span class="sxs-lookup"><span data-stu-id="02b15-106">Because multiple bits in the property value can be "on" at the same time, it is possible to use a single property value to indicate multiple concurrent values.</span></span>

<span data-ttu-id="02b15-107">Par exemple, l’exemple de code MOF suivant établit la propriété **filetype** comme avec les qualificateurs **bitmap** et **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="02b15-107">For example, the following MOF code example establishes the **FileType** property as having the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="02b15-108">Il établit en outre que le bit de poids faible (bit 0) correspond à la valeur « lecture seule ».</span><span class="sxs-lookup"><span data-stu-id="02b15-108">It further establishes that the low-order bit (bit 0) corresponds to the value "Read Only".</span></span> <span data-ttu-id="02b15-109">Le bit suivant (bit 1) correspond à « Hidden », et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="02b15-109">The next bit (bit 1) corresponds to "Hidden", and so on.</span></span> <span data-ttu-id="02b15-110">(Tous les bits ne doivent pas être significatifs.</span><span class="sxs-lookup"><span data-stu-id="02b15-110">(Not all bits must be significant.</span></span> <span data-ttu-id="02b15-111">Dans ce système huit bits, les deux bits de poids fort, 6 et 7, n’ont pas d’importance.)</span><span class="sxs-lookup"><span data-stu-id="02b15-111">In this eight-bit system, the two high-order bits, 6 and 7, have no significance.)</span></span>

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

<span data-ttu-id="02b15-112">Si la propriété **filetype** signale la valeur 7 (bits 0000 0111), le fichier est « lecture seule », « système » et « masqué ».</span><span class="sxs-lookup"><span data-stu-id="02b15-112">If the **FileType** property reports the value 7 (bits 0000 0111), the file is "Read Only", "System", and "Hidden".</span></span> <span data-ttu-id="02b15-113">Si la propriété **filetype** signale la valeur 18 (0x12, bits 0001 0010), il s’agit d’un sous-répertoire masqué.</span><span class="sxs-lookup"><span data-stu-id="02b15-113">If the **FileType** property reports the value 18 (0x12, bits 0001 0010), it is a hidden subdirectory.</span></span>

<span data-ttu-id="02b15-114">Il existe deux types de bitmaps différents utilisant le code MOF :</span><span class="sxs-lookup"><span data-stu-id="02b15-114">There are two different types of bitmaps using MOF code:</span></span>

-   <span data-ttu-id="02b15-115">Bits significatifs consécutifs commençant par le bit de poids faible (bit 0)</span><span class="sxs-lookup"><span data-stu-id="02b15-115">Consecutive significant bits beginning with the low-order bit (bit 0)</span></span>

    <span data-ttu-id="02b15-116">Vous pouvez définir un tableau de valeurs de bit sans spécifier explicitement les bits significatifs si les bits significatifs commencent par le bit de poids faible (bit 0) et progressent sans interruption sur tous les éléments du tableau **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="02b15-116">You can define an array of bit values without explicitly specifying the significant bits if the significant bits begin with the low-order bit (bit 0) and progress upward without interruption through all items in the **BitValue** array.</span></span> <span data-ttu-id="02b15-117">L’exemple de code MOF suivant exécute la même fonction que l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="02b15-117">The following MOF code example performs the same function as the previous example.</span></span>

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   <span data-ttu-id="02b15-118">Bit significatif précédé d’un bit non significatif</span><span class="sxs-lookup"><span data-stu-id="02b15-118">Significant bit preceded by a non-significant bit</span></span>

    <span data-ttu-id="02b15-119">Si le bit de poids faible n’est pas significatif, ou si la séquence de bits significatifs n’est pas continue, vous devez spécifier à la fois les qualificateurs **bitmap** et **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="02b15-119">If the low-order bit is insignificant, or the sequence of significant bits is not continuous, you must specify both the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="02b15-120">L’exemple de code MOF suivant illustre une situation dans laquelle le bit de poids faible n’est pas significatif et il y a un écart dans la séquence de bits significatifs.</span><span class="sxs-lookup"><span data-stu-id="02b15-120">The following MOF code example shows a situation in which the low-order bit is not significant and there is a gap in the sequence of significant bits.</span></span>

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    <span data-ttu-id="02b15-121">Dans ce cas, la définition du bit de poids faible (bit 0) n’a aucune signification et est ignorée.</span><span class="sxs-lookup"><span data-stu-id="02b15-121">In this case, setting the low-order bit (bit 0) has no significance and is ignored.</span></span> <span data-ttu-id="02b15-122">Toutefois, le bit 1 (0X2) indique que ce message électronique est marqué pour suivi, le paramètre de bit 4 (0x8) indique qu’un accusé de réception doit être envoyé à l’expéditeur lorsque le message électronique est arrivé à la boîte aux lettres du destinataire et que le paramètre bit 5 (0x10) spécifie qu’une confirmation de lecture doit être envoyée à l’expéditeur lorsque le destinataire ouvre le message.</span><span class="sxs-lookup"><span data-stu-id="02b15-122">However, setting bit 1 (0x2) indicates that this email message is flagged for follow up, setting bit 4 (0x8) indicates that a delivery receipt should be sent to the sender when the email message has arrived at the recipient's mailbox, and setting bit 5 (0x10) specifies that a read receipt should be sent to the sender when the email message is opened by the recipient.</span></span> <span data-ttu-id="02b15-123">La définition des trois bits significatifs (0x1A) spécifie les trois conditions pour le message électronique.</span><span class="sxs-lookup"><span data-stu-id="02b15-123">Setting all three significant bits (0x1A) specifies all three conditions for the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="02b15-124">Notes</span><span class="sxs-lookup"><span data-stu-id="02b15-124">Remarks</span></span>

<span data-ttu-id="02b15-125">Pour déterminer s’il faut utiliser les /  qualificateurs de valeurs de bitmap ou de  / **valeurs** ValueMap, déterminez si l’une des valeurs indiquées peut se produire simultanément.</span><span class="sxs-lookup"><span data-stu-id="02b15-125">In deciding whether to use the **BitMap**/**BitValues** or **ValueMap**/**Values** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="02b15-126">Si plusieurs valeurs simultanées peuvent exister, vous devez utiliser des / **bitvalues** bitmap.</span><span class="sxs-lookup"><span data-stu-id="02b15-126">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="02b15-127">Si toutes les valeurs s’excluent mutuellement, vous devez utiliser les / qualificateurs de **valeurs** ValueMap.</span><span class="sxs-lookup"><span data-stu-id="02b15-127">If all the values are mutually exclusive, you should use the **ValueMap**/**Values** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02b15-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02b15-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02b15-129">ValueMap et qualificateurs de valeur</span><span class="sxs-lookup"><span data-stu-id="02b15-129">ValueMap and Value Qualifiers</span></span>](value-map.md)
</dt> </dl>

 

 



