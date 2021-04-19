---
description: Utilisez ces instructions pour couvrir une installation Windows Installer complète par une signature numérique.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Création d’une installation signée entièrement vérifiée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e76bbfb77eab8b020cb1591847d2a36d09c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534221"
---
# <a name="authoring-a-fully-verified-signed-installation"></a><span data-ttu-id="6b840-103">Création d’une installation signée entièrement vérifiée</span><span class="sxs-lookup"><span data-stu-id="6b840-103">Authoring a Fully Verified Signed Installation</span></span>

<span data-ttu-id="6b840-104">Vous pouvez utiliser ces instructions pour couvrir une installation Windows Installer complète par une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="6b840-104">You can use these guidelines to cover an entire Windows Installer installation by a digital signature.</span></span>

<span data-ttu-id="6b840-105">Les auteurs des installations de Windows Installer doivent respecter les conditions suivantes pour s’assurer que toutes les parties de l’installation sont couvertes par une signature numérique :</span><span class="sxs-lookup"><span data-stu-id="6b840-105">Authors of Windows Installer installations must adhere to the following to ensure that all parts of the installation are covered by a digital signature:</span></span>

-   <span data-ttu-id="6b840-106">Utilisez des fichiers CAB internes ou des fichiers CAB externes signés et créez correctement la [table MsiDigitalSignature](msidigitalsignature-table.md) et la [table MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="6b840-106">Use internal cabinet files, or use signed external cabinet files and correctly author the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>
-   <span data-ttu-id="6b840-107">Utilisez uniquement des actions personnalisées stockées dans le package ou installées avec le package.</span><span class="sxs-lookup"><span data-stu-id="6b840-107">Use only custom actions stored within the package or installed with the package.</span></span>
-   <span data-ttu-id="6b840-108">Signez le package d’installation.</span><span class="sxs-lookup"><span data-stu-id="6b840-108">Sign the installation package.</span></span>
-   <span data-ttu-id="6b840-109">Incluez une [table MsiPatchCertificate](msipatchcertificate-table.md) dans le package.</span><span class="sxs-lookup"><span data-stu-id="6b840-109">Include an [MsiPatchCertificate table](msipatchcertificate-table.md) in the package.</span></span> <span data-ttu-id="6b840-110">Pour activer la mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md), cette table doit contenir les informations utilisées pour identifier les certificats de signataire utilisés pour signer numériquement les correctifs.</span><span class="sxs-lookup"><span data-stu-id="6b840-110">To enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md), this table must contain information used to identify the signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="6b840-111">La mise à jour corrective du contrôle de compte d’utilisateur permet à l’auteur du package d’installation d’identifier les correctifs signés numériquement qui peuvent être appliqués ultérieurement par des utilisateurs non-administrateurs.</span><span class="sxs-lookup"><span data-stu-id="6b840-111">UAC patching enables the author of the installation package to identify digitally-signed patches that can be applied in the future by non-administrator users.</span></span>

<span data-ttu-id="6b840-112">Pour obtenir un exemple illustrant comment créer une installation signée à l’aide d’Automation, consultez [création d’une installation signée entièrement vérifiée à l’aide d’Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="6b840-112">For an example showing how to author a signed installation using automation, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

 

 



