---
description: La \_ méthode GetObjectText de l’objet SWbemLastError retourne un rendu textuel de l’objet au Format format MOF (MOF).
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: Méthode SWbemLastError.GetObjectText_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952155"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a><span data-ttu-id="a640c-103">Méthode SWbemLastError. GetObjectText \_</span><span class="sxs-lookup"><span data-stu-id="a640c-103">SWbemLastError.GetObjectText\_ method</span></span>

<span data-ttu-id="a640c-104">La **méthode \_ GetObjectText** de l’objet [**SWbemLastError**](swbemlasterror.md) retourne un rendu textuel de l’objet au format [format MOF (MOF)](managed-object-format--mof-.md) .</span><span class="sxs-lookup"><span data-stu-id="a640c-104">The **GetObjectText\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a textual rendering of the object in a [Managed Object Format (MOF)](managed-object-format--mof-.md) format.</span></span> <span data-ttu-id="a640c-105">Cet objet MOF peut être utilisé pour afficher le contenu d’un objet.</span><span class="sxs-lookup"><span data-stu-id="a640c-105">This MOF object can be used to display an object's contents.</span></span> <span data-ttu-id="a640c-106">Notez que le texte MOF qui est retourné ne contient pas toutes les informations relatives à l’objet, mais uniquement les informations nécessaires au compilateur MOF pour pouvoir recréer l’objet d’origine.</span><span class="sxs-lookup"><span data-stu-id="a640c-106">Notice that the MOF text that is returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="a640c-107">Par exemple, vous ne trouverez aucune information sur les qualificateurs propagés ou les propriétés de la classe parente.</span><span class="sxs-lookup"><span data-stu-id="a640c-107">For instance, you will not find any information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="a640c-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a640c-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a640c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a640c-109">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a640c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a640c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a640c-111">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a640c-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a640c-112">Ce paramètre est réservé et doit avoir la valeur 0 (zéro) s’il est spécifié.</span><span class="sxs-lookup"><span data-stu-id="a640c-112">This parameter is reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a640c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a640c-113">Return value</span></span>

<span data-ttu-id="a640c-114">En cas de réussite, cette méthode retourne une chaîne qui contient le texte de sortie.</span><span class="sxs-lookup"><span data-stu-id="a640c-114">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a640c-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a640c-115">Error codes</span></span>

<span data-ttu-id="a640c-116">À la fin de la **méthode \_ GetObjectText** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="a640c-116">Upon the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a640c-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a640c-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a640c-118">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a640c-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a640c-119">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a640c-119">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a640c-120">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a640c-120">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a640c-121">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a640c-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a640c-122">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a640c-122">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a640c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a640c-123">Requirements</span></span>



| <span data-ttu-id="a640c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a640c-124">Requirement</span></span> | <span data-ttu-id="a640c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a640c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a640c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a640c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a640c-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a640c-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a640c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a640c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a640c-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a640c-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a640c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="a640c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a640c-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a640c-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a640c-132">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a640c-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="a640c-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a640c-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a640c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a640c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a640c-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a640c-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a640c-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="a640c-136">CLSID</span></span><br/>                    | <span data-ttu-id="a640c-137">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="a640c-137">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="a640c-138">IID</span><span class="sxs-lookup"><span data-stu-id="a640c-138">IID</span></span><br/>                      | <span data-ttu-id="a640c-139">IID \_ ISWbemLastError</span><span class="sxs-lookup"><span data-stu-id="a640c-139">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




