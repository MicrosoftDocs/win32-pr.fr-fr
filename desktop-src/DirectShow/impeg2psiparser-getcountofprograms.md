---
description: L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'IMpeg2PsiParser :: GetCountOfPrograms, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: e4f01b2a360465b9670b52547cff1ff4c312a705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846501"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="9d388-104">IMpeg2PsiParser :: GetCountOfPrograms, méthode</span><span class="sxs-lookup"><span data-stu-id="9d388-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="9d388-105">L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9d388-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="9d388-106">Il ne s’agit pas d’une API DirectShow prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9d388-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="9d388-107">La `GetCountOfPrograms` méthode récupère le nombre de programmes dans le flux de transport.</span><span class="sxs-lookup"><span data-stu-id="9d388-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d388-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d388-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="9d388-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d388-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d388-110">*pNumOfPrograms* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9d388-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d388-111">Pointeur vers une variable qui reçoit le nombre de programmes.</span><span class="sxs-lookup"><span data-stu-id="9d388-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d388-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d388-112">Return value</span></span>

<span data-ttu-id="9d388-113">La méthode retourne une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="9d388-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="9d388-114">Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9d388-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="9d388-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9d388-115">Return code</span></span>                                                                          | <span data-ttu-id="9d388-116">Description</span><span class="sxs-lookup"><span data-stu-id="9d388-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="9d388-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d388-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9d388-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="9d388-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9d388-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d388-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d388-120">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="9d388-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="9d388-121">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="9d388-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




