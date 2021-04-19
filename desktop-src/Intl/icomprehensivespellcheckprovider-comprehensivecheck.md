---
description: 'Vérifiez l’orthographe du texte du fournisseur de manière plus approfondie que ISpellCheckProvider :: Check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'IComprehensiveSpellCheckProvider :: ComprehensiveCheck, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522463"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a><span data-ttu-id="8c7ef-103">IComprehensiveSpellCheckProvider :: ComprehensiveCheck, méthode</span><span class="sxs-lookup"><span data-stu-id="8c7ef-103">IComprehensiveSpellCheckProvider::ComprehensiveCheck method</span></span>

<span data-ttu-id="8c7ef-104">Vérifiez l’orthographe du texte du fournisseur de manière plus approfondie que [**ISpellCheckProvider :: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="8c7ef-104">Spell-check the provider text in a more thorough manner than [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c7ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c7ef-105">Syntax</span></span>


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a><span data-ttu-id="8c7ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c7ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c7ef-107">*texte* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c7ef-107">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c7ef-108">Texte à vérifier.</span><span class="sxs-lookup"><span data-stu-id="8c7ef-108">The text to check.</span></span>

</dd> <dt>

<span data-ttu-id="8c7ef-109">*résultat* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8c7ef-109">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c7ef-110">Résultat de la vérification de ce texte, sous la forme d’une énumération des fautes d’orthographe ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="8c7ef-110">The result of checking this text, as an enumeration of spelling errors ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c7ef-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c7ef-111">Return value</span></span>

<span data-ttu-id="8c7ef-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8c7ef-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8c7ef-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c7ef-113">Return value</span></span>                                                                             | <span data-ttu-id="8c7ef-114">Description</span><span class="sxs-lookup"><span data-stu-id="8c7ef-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8c7ef-115"><dt>\_OK</dt></span><span class="sxs-lookup"><span data-stu-id="8c7ef-115"><dt>S\_OK</dt></span></span> </dl>         | <span data-ttu-id="8c7ef-116">Vendu.</span><span class="sxs-lookup"><span data-stu-id="8c7ef-116">Successful.</span></span><br/>                |
| <dl> <span data-ttu-id="8c7ef-117"><dt>E \_ INVALIDARG</dt></span><span class="sxs-lookup"><span data-stu-id="8c7ef-117"><dt>E\_INVALIDARG</dt></span></span> </dl> | <span data-ttu-id="8c7ef-118">le *texte* est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="8c7ef-118">*text* is an empty string.</span></span><br/> |
| <dl> <span data-ttu-id="8c7ef-119"><dt>\_pointeur E</dt></span><span class="sxs-lookup"><span data-stu-id="8c7ef-119"><dt>E\_POINTER</dt></span></span> </dl>    | <span data-ttu-id="8c7ef-120">le *texte* est un pointeur null.</span><span class="sxs-lookup"><span data-stu-id="8c7ef-120">*text* is a null pointer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="8c7ef-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8c7ef-121">Remarks</span></span>

<span data-ttu-id="8c7ef-122">Cette interface n’est pas obligatoire pour être implémentée par un fournisseur de vérification orthographique.</span><span class="sxs-lookup"><span data-stu-id="8c7ef-122">This interface isn't required to be implemented by a spell check provider.</span></span> <span data-ttu-id="8c7ef-123">Toutefois, si le fournisseur prend en charge deux « modes » de vérification orthographique (plus rapide et plus rapide, mais plus complet), il doit implémenter cette interface dans le même objet qui implémente [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) pour prendre en charge le mode de vérification plus approfondi.</span><span class="sxs-lookup"><span data-stu-id="8c7ef-123">But if the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it should implement this interface in the same object that implements [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) to support the more thorough checking mode.</span></span> <span data-ttu-id="8c7ef-124">Lorsqu’un client appelle [**des :: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), la fonctionnalité de vérification orthographique effectue une opération [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour le fournisseur de [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)et appelle **IComprehensiveSpellCheckProvider. ComprehensiveCheck** si l’interface est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8c7ef-124">When a client calls [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), the spell checking functionality will [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) the provider for [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider), and call **IComprehensiveSpellCheckProvider.ComprehensiveCheck** if the interface is supported.</span></span> <span data-ttu-id="8c7ef-125">Si l’interface n’est pas prise en charge, elle revient silencieusement à [**ISpellCheckProvider :: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="8c7ef-125">If the interface isn't supported, it will silently fall back to [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="see-also"></a><span data-ttu-id="8c7ef-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c7ef-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c7ef-127">**IComprehensiveSpellCheckProvider**</span><span class="sxs-lookup"><span data-stu-id="8c7ef-127">**IComprehensiveSpellCheckProvider**</span></span>](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[<span data-ttu-id="8c7ef-128">**IEnumSpellingError**</span><span class="sxs-lookup"><span data-stu-id="8c7ef-128">**IEnumSpellingError**</span></span>](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[<span data-ttu-id="8c7ef-129">**Des :: ComprehensiveCheck**</span><span class="sxs-lookup"><span data-stu-id="8c7ef-129">**ISpellChecker::ComprehensiveCheck**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[<span data-ttu-id="8c7ef-130">**ISpellCheckProvider**</span><span class="sxs-lookup"><span data-stu-id="8c7ef-130">**ISpellCheckProvider**</span></span>](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[<span data-ttu-id="8c7ef-131">**ISpellCheckProvider :: Check**</span><span class="sxs-lookup"><span data-stu-id="8c7ef-131">**ISpellCheckProvider::Check**</span></span>](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
