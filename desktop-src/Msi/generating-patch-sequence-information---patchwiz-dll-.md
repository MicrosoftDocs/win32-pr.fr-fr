---
description: La version de PATCHWIZ.DLL publiée avec Windows Installer&\# 160 ; 3.0 peut générer automatiquement des informations de séquencement de correctifs et ajouter à la table MsiPatchSequence un nouveau correctif.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Génération d’informations sur les séquences de correctifs (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff82166f33266a58cd3ef299b2546b04a94ebb14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952296"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a><span data-ttu-id="68e68-103">Génération d’informations sur les séquences de correctifs (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="68e68-103">Generating Patch Sequence Information (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="68e68-104">La version de [PATCHWIZ.DLL](patchwiz-dll.md) publiée avec Windows Installer 3,0 peut générer automatiquement des informations de séquencement de correctifs et ajouter à la [table MsiPatchSequence](msipatchsequence-table.md) un nouveau correctif.</span><span class="sxs-lookup"><span data-stu-id="68e68-104">The version of [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 can automatically generate patch sequencing information and add to the [MsiPatchSequence Table](msipatchsequence-table.md) a new patch.</span></span>

<span data-ttu-id="68e68-105">Définissez la \_ \_ propriété de génération de données \_ de séquence désactivé sur 1 (un) dans la [table de propriétés](properties-table-patchwiz-dll-.md) du fichier. PCP pour empêcher la génération automatique des informations de séquencement de correctifs.</span><span class="sxs-lookup"><span data-stu-id="68e68-105">Set the SEQUENCE\_DATA\_GENERATION\_DISABLED property to 1 (one) in the [Properties Table](properties-table-patchwiz-dll-.md) of the .pcp file to prevent the automatic generation of patch sequencing information.</span></span> <span data-ttu-id="68e68-106">Si cette propriété est absente, les informations sont automatiquement générées et ajoutées.</span><span class="sxs-lookup"><span data-stu-id="68e68-106">If this property is absent, the information is automatically generated and added.</span></span>

<span data-ttu-id="68e68-107">Lorsque le [PATCHWIZ.DLL](patchwiz-dll.md) fourni avec Windows Installer 3,0 est utilisé pour générer automatiquement les informations de séquencement des correctifs, voici ce qui se produit :</span><span class="sxs-lookup"><span data-stu-id="68e68-107">When the [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 is used to automatically generate the patch sequencing information, the following occurs:</span></span>

-   <span data-ttu-id="68e68-108">Une nouvelle ligne est ajoutée à la [table MsiPatchSequence](msipatchsequence-table.md) pour chaque code de produit d’une image cible qui est indiquée dans la [table TargetImages](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="68e68-108">A new row is added to the [MsiPatchSequence Table](msipatchsequence-table.md) for each product code of a target image that is listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="68e68-109">Les valeurs ajoutées à la colonne PatchFamily dans les nouvelles lignes correspondent aux codes de produit cibles des images cibles qui sont répertoriées dans la [table TargetImages](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="68e68-109">The values added to the PatchFamily column in the new rows correspond to the target product codes of the target images that are listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="68e68-110">Les valeurs ajoutées aux colonnes de séquence dans les nouvelles lignes sont générées à l’aide de la version de produit la plus élevée ciblée par le correctif et de l’heure UTC à laquelle le correctif est généré.</span><span class="sxs-lookup"><span data-stu-id="68e68-110">The values added to the Sequence columns in the new rows are generated using the highest product version targeted by the patch and the UTC time when the patch is generated.</span></span> <span data-ttu-id="68e68-111">Le numéro de séquence est <Product Minor Version> . <Build Major Number> . <horodatage 1>. <horodatage 2>.</span><span class="sxs-lookup"><span data-stu-id="68e68-111">The sequence number is <Product Minor Version>.<Build Major Number>.<Time Stamp 1>.<Time Stamp 2>.</span></span>
    -   <span data-ttu-id="68e68-112">Le premier champ correspond à la version du produit de la version la plus récente du produit ciblée par le correctif.</span><span class="sxs-lookup"><span data-stu-id="68e68-112">The first field is the product version of the highest version of the product that is targeted by the patch.</span></span>
    -   <span data-ttu-id="68e68-113">Le deuxième champ est le numéro principal de la version la plus récente du produit ciblé par le correctif.</span><span class="sxs-lookup"><span data-stu-id="68e68-113">The second field is the build major number of the highest version of the product that is targeted by the patch.</span></span>

    <span data-ttu-id="68e68-114">Les deux champs d’horodatage pour l’horodatage de 32 bits, qui est nécessaire pour compter les secondes en temps universel coordonné (UTC, Universal Time Coordinated).</span><span class="sxs-lookup"><span data-stu-id="68e68-114">The two time stamp fields account for the 32 bit time stamp that is needed to count the seconds in Coordinated Universal Time (UTC).</span></span>
    > [!Note]  
    > <span data-ttu-id="68e68-115">Les versions du produit ont le format suivant : <Product Major Version> .. <Product Minor Version> <Build Major Number> . <Build Minor Number> et un produit avec un numéro de version 2.1.0.0 est une version supérieure à celle d’un produit avec le numéro de version 1.2.0.0</span><span class="sxs-lookup"><span data-stu-id="68e68-115">Product versions have the following format: <Product Major Version>.<Product Minor Version>.<Build Major Number>.<Build Minor Number> and a product with a version number 2.1.0.0 is a higher version than a product with version number 1.2.0.0</span></span>

     

-   <span data-ttu-id="68e68-116">L’attribut msidbPatchSequenceSupersedeEarlier est entré dans la colonne attribut des nouvelles lignes générées pour les service packs (SP) ou les correctifs de mise à niveau mineure.</span><span class="sxs-lookup"><span data-stu-id="68e68-116">The msidbPatchSequenceSupersedeEarlier attribute is entered into the Attribute column of new rows that are generated for service packs (SP) or minor upgrade patches.</span></span> <span data-ttu-id="68e68-117">L’attribut msidbPatchSequenceSupersedeEarlier n’est pas ajouté à un correctif QFE ou à une mise à jour de petite taille.</span><span class="sxs-lookup"><span data-stu-id="68e68-117">The msidbPatchSequenceSupersedeEarlier attribute is not added to a QFE or small update patch.</span></span>
    > [!Note]  
    > <span data-ttu-id="68e68-118">Un Service Pack (SP) doit contenir les correctifs de tous les correctifs qui ont été publiés avant celui-ci.</span><span class="sxs-lookup"><span data-stu-id="68e68-118">A service pack (SP) should contain the fixes of all the QFEs that were released prior to it.</span></span> <span data-ttu-id="68e68-119">Toutefois, si un auteur de correctif définit la \_ propriété de remplacement des données de séquence \_ sur 0 (zéro) ou 1 (un) dans le fichier. PCP, la colonne attributs de toutes les lignes de la table MsiPatchSequence est définie sur la valeur spécifiée pour le remplacement des données de séquence \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="68e68-119">However, if a patch author sets the SEQUENCE\_DATA\_SUPERSEDENCE property to 0 (zero) or 1 (one) in the .pcp file, the Attributes column of all rows in the MsiPatchSequence table is set to the value that is specified for SEQUENCE\_DATA\_SUPERSEDENCE.</span></span> <span data-ttu-id="68e68-120">Les auteurs de correctifs qui requièrent davantage de contrôle doivent créer manuellement la colonne d’attributs.</span><span class="sxs-lookup"><span data-stu-id="68e68-120">Patch authors who require more control must author the Attributes column manually.</span></span>

     

<span data-ttu-id="68e68-121">Si vous incluez une [table PatchSequence](patchsequence-table--patchwiz-dll-.md) dans le fichier. PCP, la \_ \_ propriété de génération de données de séquence \_ désactivée est ignorée et les informations fournies dans la table PatchSequence peuvent être ajoutées à la [table MsiPatchSequence](msipatchsequence-table.md) du correctif.</span><span class="sxs-lookup"><span data-stu-id="68e68-121">If you include a [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) in the .pcp file, the SEQUENCE\_DATA\_GENERATION\_DISABLED property is ignored and the information provided in the PatchSequence Table can be added to the [MsiPatchSequence Table](msipatchsequence-table.md) of the patch.</span></span>

 

 



