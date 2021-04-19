---
description: Définit ou récupère une valeur booléenne qui spécifie si les invites de l’interface utilisateur pour l’identité de l’expéditeur ou du signataire peuvent être utilisées.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Propriété Settings. EnablePromptForCertificateUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537988"
---
# <a name="settingsenablepromptforcertificateui-property"></a><span data-ttu-id="9a183-103">Propriété Settings. EnablePromptForCertificateUI</span><span class="sxs-lookup"><span data-stu-id="9a183-103">Settings.EnablePromptForCertificateUI property</span></span>

<span data-ttu-id="9a183-104">\[La propriété **EnablePromptForCertificateUI** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.\]</span><span class="sxs-lookup"><span data-stu-id="9a183-104">\[The **EnablePromptForCertificateUI** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="9a183-105">La propriété **EnablePromptForCertificateUI** définit ou récupère une valeur booléenne qui spécifie si les invites de l’interface utilisateur pour l’identité de l’expéditeur ou du signataire peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="9a183-105">The **EnablePromptForCertificateUI** property sets or retrieves a Boolean value that specifies whether user interface prompts for a signer or sender's identity can be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a183-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a183-106">Syntax</span></span>


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a><span data-ttu-id="9a183-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9a183-107">Property value</span></span>

<span data-ttu-id="9a183-108">Si la **valeur est true**, les invites de l’interface utilisateur pour l’identité de l’expéditeur ou du signataire peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="9a183-108">If **true**, user interface prompts for a signer or sender's identity can be used.</span></span> <span data-ttu-id="9a183-109">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="9a183-109">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="9a183-110">La définition de cette propriété ne désactive pas les avertissements générés avant l’utilisation d’une clé privée à partir d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="9a183-110">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a183-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a183-111">Requirements</span></span>



| <span data-ttu-id="9a183-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a183-112">Requirement</span></span> | <span data-ttu-id="9a183-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a183-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a183-114">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="9a183-114">Redistributable</span></span><br/> | <span data-ttu-id="9a183-115">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a183-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9a183-116">DLL</span><span class="sxs-lookup"><span data-stu-id="9a183-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="9a183-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a183-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a183-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a183-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a183-119">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="9a183-119">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




