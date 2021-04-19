---
description: Cette section fournit la liste des codes de retour WMI, des constantes symboliques, des valeurs littérales et des descriptions. Ces codes peuvent être renvoyés par des scripts, des applications C++ ou des commandes WMIC.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Codes de retour WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521485"
---
# <a name="wmi-return-codes"></a><span data-ttu-id="ecc3e-104">Codes de retour WMI</span><span class="sxs-lookup"><span data-stu-id="ecc3e-104">WMI Return Codes</span></span>

<span data-ttu-id="ecc3e-105">Cette section fournit la liste des codes de retour WMI, des constantes symboliques, des valeurs littérales et des descriptions.</span><span class="sxs-lookup"><span data-stu-id="ecc3e-105">This section provides a list of the WMI return codes, symbolic constants, literal values, and descriptions.</span></span> <span data-ttu-id="ecc3e-106">Ces codes peuvent être renvoyés par des scripts, des applications C++ ou des commandes [**WMIC**](wmic.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc3e-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md) commands.</span></span>

<span data-ttu-id="ecc3e-107">Si une erreur se produit, WMI retourne l’un des codes d’erreur suivants sous la forme d’une valeur 32 bits où les deux bits de poids fort indiquent le code de gravité du message.</span><span class="sxs-lookup"><span data-stu-id="ecc3e-107">If an error occurs, WMI returns one of the following error codes as a 32-bit value where the two high-order bits indicate the severity code of the message.</span></span>

<dl> <dt>

<span data-ttu-id="ecc3e-108"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="ecc3e-108"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="ecc3e-109">Succès</span><span class="sxs-lookup"><span data-stu-id="ecc3e-109">Success</span></span>

</dd> <dt>

<span data-ttu-id="ecc3e-110"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="ecc3e-110"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="ecc3e-111">Informationnel</span><span class="sxs-lookup"><span data-stu-id="ecc3e-111">Informational</span></span>

</dd> <dt>

<span data-ttu-id="ecc3e-112"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="ecc3e-112"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="ecc3e-113">Avertissement</span><span class="sxs-lookup"><span data-stu-id="ecc3e-113">Warning</span></span>

</dd> <dt>

<span data-ttu-id="ecc3e-114"><span id="3"></span>1,3</span><span class="sxs-lookup"><span data-stu-id="ecc3e-114"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="ecc3e-115">Error</span><span class="sxs-lookup"><span data-stu-id="ecc3e-115">Error</span></span>

</dd> </dl>

> [!Note]
>
> <span data-ttu-id="ecc3e-116">Si WMI renvoie des messages d’erreur, sachez qu’ils ne peuvent pas indiquer des problèmes dans le service WMI ou les fournisseurs WMI.</span><span class="sxs-lookup"><span data-stu-id="ecc3e-116">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="ecc3e-117">Les échecs peuvent provenir d’autres parties du système d’exploitation et émerger comme des erreurs via WMI.</span><span class="sxs-lookup"><span data-stu-id="ecc3e-117">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="ecc3e-118">Dans tous les cas, ne supprimez pas le référentiel WMI en tant que première action, car la suppression du dépôt peut endommager le système ou les applications installées.</span><span class="sxs-lookup"><span data-stu-id="ecc3e-118">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="ecc3e-119">Pour obtenir plus d’informations sur la source du problème, vous pouvez télécharger et exécuter l’outil en ligne de commande [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic.</span><span class="sxs-lookup"><span data-stu-id="ecc3e-119">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="ecc3e-120">Cet outil génère un rapport qui peut généralement isoler la source du problème et fournir des instructions sur la façon de le résoudre.</span><span class="sxs-lookup"><span data-stu-id="ecc3e-120">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="ecc3e-121">Le rapport aide également les services de support technique Microsoft à vous aider.</span><span class="sxs-lookup"><span data-stu-id="ecc3e-121">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="ecc3e-122">Vous pouvez télécharger les WMI Diagnosis Utility [ici](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="ecc3e-122">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

-   [<span data-ttu-id="ecc3e-123">**Constantes d’erreur WMI**</span><span class="sxs-lookup"><span data-stu-id="ecc3e-123">**WMI Error Constants**</span></span>](wmi-error-constants.md)
-   [<span data-ttu-id="ecc3e-124">**Constantes non-erreur WMI**</span><span class="sxs-lookup"><span data-stu-id="ecc3e-124">**WMI Non-Error Constants**</span></span>](wmi-non-error-constants.md)

 

 



