---
description: L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.
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
ms.openlocfilehash: 6117060cf0c8d3c56d03e5838376485244fde8d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392448"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="29a95-104">IMpeg2PsiParser :: GetPatVersionNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="29a95-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="29a95-105">L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="29a95-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="29a95-106">Il ne s’agit pas d’une API DirectShow prise en charge.</span><span class="sxs-lookup"><span data-stu-id="29a95-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="29a95-107">La `GetPatVersionNumber` méthode récupère le champ du \_ numéro de version à partir de Pat.</span><span class="sxs-lookup"><span data-stu-id="29a95-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="29a95-108">Un flux de transport contient au plus un PAT.</span><span class="sxs-lookup"><span data-stu-id="29a95-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="29a95-109">Le numéro de version est incrémenté chaque fois que les informations de la table sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="29a95-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="29a95-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29a95-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="29a95-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29a95-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29a95-112">*pPatVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="29a95-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29a95-113">Pointeur vers une variable qui reçoit le champ du numéro de version \_ .</span><span class="sxs-lookup"><span data-stu-id="29a95-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29a95-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29a95-114">Return value</span></span>

<span data-ttu-id="29a95-115">La méthode retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29a95-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="29a95-116">Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="29a95-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="29a95-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="29a95-117">Return code</span></span>                                                                          | <span data-ttu-id="29a95-118">Description</span><span class="sxs-lookup"><span data-stu-id="29a95-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="29a95-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="29a95-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="29a95-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="29a95-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="29a95-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29a95-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29a95-122">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="29a95-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="29a95-123">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="29a95-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




