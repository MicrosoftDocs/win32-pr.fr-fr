---
description: Windows Installer fonctions qui retournent des données dans un emplacement de mémoire fourni par l’utilisateur ne doivent pas être appelées avec NULL comme valeur pour le pointeur.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Passage de la valeur null aux fonctions Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521469"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a><span data-ttu-id="ac44f-103">Passage de NULL comme argument des fonctions Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ac44f-103">Passing null as the Argument of Windows Installer Functions</span></span>

<span data-ttu-id="ac44f-104">Windows Installer fonctions qui retournent des données dans un emplacement de mémoire fourni par l’utilisateur ne doivent pas être appelées avec NULL comme valeur pour le pointeur.</span><span class="sxs-lookup"><span data-stu-id="ac44f-104">Windows Installer functions that return data in a user provided–memory location should not be called with null as the value for the pointer.</span></span> <span data-ttu-id="ac44f-105">Ces fonctions retournent une chaîne ou retournent des données sous forme de pointeurs entiers, mais retournent des valeurs incohérentes lors du passage de NULL comme valeur de l’argument de sortie.</span><span class="sxs-lookup"><span data-stu-id="ac44f-105">These functions return a string or return data as integer pointers, but return inconsistent values when passing null as the value for the output argument.</span></span>

<span data-ttu-id="ac44f-106">Ne transmettez pas NULL comme valeur de l’argument de sortie pour l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac44f-106">Do not pass Null as the value of the output argument for any of the following functions:</span></span>

[<span data-ttu-id="ac44f-107">**MsiGetProperty**</span><span class="sxs-lookup"><span data-stu-id="ac44f-107">**MsiGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[<span data-ttu-id="ac44f-108">**MsiRecordGetString**</span><span class="sxs-lookup"><span data-stu-id="ac44f-108">**MsiRecordGetString**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[<span data-ttu-id="ac44f-109">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="ac44f-109">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[<span data-ttu-id="ac44f-110">**MsiGetSourcePath**</span><span class="sxs-lookup"><span data-stu-id="ac44f-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[<span data-ttu-id="ac44f-111">**MsiGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="ac44f-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[<span data-ttu-id="ac44f-112">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="ac44f-112">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="ac44f-113">**MsiViewGetError**</span><span class="sxs-lookup"><span data-stu-id="ac44f-113">**MsiViewGetError**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[<span data-ttu-id="ac44f-114">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="ac44f-114">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[<span data-ttu-id="ac44f-115">**MsiEvaluateCondition**</span><span class="sxs-lookup"><span data-stu-id="ac44f-115">**MsiEvaluateCondition**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[<span data-ttu-id="ac44f-116">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="ac44f-116">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="ac44f-117">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="ac44f-117">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="ac44f-118">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="ac44f-118">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[<span data-ttu-id="ac44f-119">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="ac44f-119">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="ac44f-120">**MsiGetFeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="ac44f-120">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



