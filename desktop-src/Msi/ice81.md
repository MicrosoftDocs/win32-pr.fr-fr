---
description: ICE81 valide la table MsiDigitalCertificate, la table MsiDigitalSignature, la table MsiPatchCertificate et la table MsiPackageCertificate.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752789"
---
# <a name="ice81"></a><span data-ttu-id="41655-103">ICE81</span><span class="sxs-lookup"><span data-stu-id="41655-103">ICE81</span></span>

<span data-ttu-id="41655-104">ICE81 valide la table [MsiDigitalCertificate](msidigitalcertificate-table.md), la table [MsiDigitalSignature](msidigitalsignature-table.md), la table [MsiPatchCertificate](msipatchcertificate-table.md)et la [table MsiPackageCertificate](msipackagecertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="41655-104">ICE81 validates the [MsiDigitalCertificate table](msidigitalcertificate-table.md), [MsiDigitalSignature table](msidigitalsignature-table.md), [MsiPatchCertificate table](msipatchcertificate-table.md), and [MsiPackageCertificate Table](msipackagecertificate-table.md).</span></span> <span data-ttu-id="41655-105">Cette action personnalisée ICE publie des avertissements pour les certificats numériques qui sont inutilisés ou non référencés, et publie une erreur lorsque l’objet signé n’existe pas ou lorsque le cabinet de l’objet signé ne pointe pas vers des données externes.</span><span class="sxs-lookup"><span data-stu-id="41655-105">This ICE custom action posts warnings for digital certificates that are unused or unreferenced, and it posts an error when the signed object does not exist or when the signed object's cabinet does not point to external data.</span></span>

<span data-ttu-id="41655-106">Notez que ICE03 vérifie que l’entrée dans la colonne de table de la table MsiDigitalSignature est « Media ».</span><span class="sxs-lookup"><span data-stu-id="41655-106">Note that ICE03 verifies that the entry in the Table column in the MsiDigitalSignature table is "Media."</span></span>

## <a name="result"></a><span data-ttu-id="41655-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="41655-107">Result</span></span>

<span data-ttu-id="41655-108">ICE81 publie les avertissements suivants pour les certificats numériques non utilisés ou non référencés.</span><span class="sxs-lookup"><span data-stu-id="41655-108">ICE81 posts the following warnings for unused or unreferenced Digital Certificates.</span></span>



| <span data-ttu-id="41655-109">AVERTISSEMENT ICE81</span><span class="sxs-lookup"><span data-stu-id="41655-109">ICE81 warning</span></span>                                                                                                                                                      | <span data-ttu-id="41655-110">Description</span><span class="sxs-lookup"><span data-stu-id="41655-110">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="41655-111">Aucune référence à l’un des enregistrements de la table MsiDigitalCertificate n’a été trouvée dans les tables MsiDigitalSignature, MsiPackageCertificate ou MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="41655-111">No reference to any of the records in the MsiDigitalCertificate table could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span> | <span data-ttu-id="41655-112">Cet avertissement est retourné si tous les enregistrements sont inutilisés.</span><span class="sxs-lookup"><span data-stu-id="41655-112">This warning is returned if all records are unused.</span></span>                |
| <span data-ttu-id="41655-113">Aucune référence au certificat numérique \[ 1 \] n’a été trouvée dans les tables MsiDigitalSignature, MsiPackageCertificate ou MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="41655-113">No reference to the Digital Certificate \[1\] could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span>                         | <span data-ttu-id="41655-114">Cet avertissement est retourné si certains enregistrements, mais pas tous, ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="41655-114">This warning is returned if some records, but not all, are unused.</span></span> |



 

<span data-ttu-id="41655-115">ICE81 publie les erreurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="41655-115">ICE81 posts the following errors.</span></span>



| <span data-ttu-id="41655-116">Erreur ICE81</span><span class="sxs-lookup"><span data-stu-id="41655-116">ICE81 error</span></span>                                                                                                                                                              | <span data-ttu-id="41655-117">Description</span><span class="sxs-lookup"><span data-stu-id="41655-117">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41655-118">La table multimédia n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="41655-118">Media Table does not exist.</span></span> <span data-ttu-id="41655-119">Par conséquent, toutes les entrées dans MsiDigitalSignature sont incorrectes</span><span class="sxs-lookup"><span data-stu-id="41655-119">Hence all the entries in MsiDigitalSignature are incorrect</span></span>                                                                                   | <span data-ttu-id="41655-120">L’objet signé n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="41655-120">The signed object does not exist.</span></span> <span data-ttu-id="41655-121">Cette erreur est retournée si la table de média n’existe pas mais que MsiDigitalSignature a des entrées.</span><span class="sxs-lookup"><span data-stu-id="41655-121">This error is returned if the Media table does not exist but MsiDigitalSignature has entries.</span></span>                                |
| <span data-ttu-id="41655-122">Objet signé manquant \[ 2 \] dans la table multimédia</span><span class="sxs-lookup"><span data-stu-id="41655-122">Missing signed object \[2\] in Media Table</span></span>                                                                                                                               | <span data-ttu-id="41655-123">L’objet signé \[ 2 \] n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="41655-123">The signed object \[2\] does not exist.</span></span> <span data-ttu-id="41655-124">Cette erreur est retournée si la table de supports existe, mais que cette entrée dans MsiDigitalSignature n’est pas présente dans la table des médias.</span><span class="sxs-lookup"><span data-stu-id="41655-124">This error is returned if the Media table exists, but this entry in MsiDigitalSignature is not present in Media table.</span></span> |
| <span data-ttu-id="41655-125">L’entrée dans le tableau \[ 1 \] avec la clé \[ 2 \] est signée.</span><span class="sxs-lookup"><span data-stu-id="41655-125">The entry in table \[1\] with key \[2\] is signed.</span></span> <span data-ttu-id="41655-126">Par conséquent, l’armoire doit pointer vers un objet situé en dehors du package (la valeur du cabinet ne doit pas être préfixée \# )</span><span class="sxs-lookup"><span data-stu-id="41655-126">Hence the cabinet should point to an object outside the package (the value of Cabinet should NOT be prefixed with \#)</span></span> | <span data-ttu-id="41655-127">Le cabinet de l’objet signé ne pointe pas vers des données externes.</span><span class="sxs-lookup"><span data-stu-id="41655-127">The signed object's cabinet does not point to external data.</span></span> <span data-ttu-id="41655-128">\[1 \] est un nom de table.</span><span class="sxs-lookup"><span data-stu-id="41655-128">\[1\] is table name.</span></span> <span data-ttu-id="41655-129">\[2 \] est la clé de la table des médias.</span><span class="sxs-lookup"><span data-stu-id="41655-129">\[2\] is key in the Media table.</span></span>                                             |



 

## <a name="related-topics"></a><span data-ttu-id="41655-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41655-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41655-131">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="41655-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



