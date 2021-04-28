---
description: 'IMpeg2PsiParser :: GetPatVersionNumber, méthode-l’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.'
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: 'IMpeg2PsiParser :: GetPatVersionNumber, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 978da4c7076bcf8ffe91bc2b9a4b2077d9d3d48a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089147"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="1f9e4-104">IMpeg2PsiParser :: GetPatVersionNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="1f9e4-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="1f9e4-105">L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="1f9e4-106">Il ne s’agit pas d’une API DirectShow prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="1f9e4-107">La `GetPatVersionNumber` méthode récupère le champ du \_ numéro de version à partir de Pat.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="1f9e4-108">Un flux de transport contient au plus un PAT.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="1f9e4-109">Le numéro de version est incrémenté chaque fois que les informations de la table sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f9e4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f9e4-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="1f9e4-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f9e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f9e4-112">*pPatVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1f9e4-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f9e4-113">Pointeur vers une variable qui reçoit le champ du numéro de version \_ .</span><span class="sxs-lookup"><span data-stu-id="1f9e4-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f9e4-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f9e4-114">Return value</span></span>

<span data-ttu-id="1f9e4-115">La méthode retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f9e4-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="1f9e4-116">Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="1f9e4-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1f9e4-117">Return code</span></span>                                                                          | <span data-ttu-id="1f9e4-118">Description</span><span class="sxs-lookup"><span data-stu-id="1f9e4-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="1f9e4-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f9e4-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1f9e4-120">Réussite.</span><span class="sxs-lookup"><span data-stu-id="1f9e4-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1f9e4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f9e4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9e4-122">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="1f9e4-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="1f9e4-123">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="1f9e4-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




