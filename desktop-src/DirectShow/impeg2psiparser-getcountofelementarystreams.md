---
description: L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'IMpeg2PsiParser :: GetCountOfElementaryStreams, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106543066"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="77382-104">IMpeg2PsiParser :: GetCountOfElementaryStreams, méthode</span><span class="sxs-lookup"><span data-stu-id="77382-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="77382-105">L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="77382-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="77382-106">Il ne s’agit pas d’une API DirectShow prise en charge.</span><span class="sxs-lookup"><span data-stu-id="77382-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="77382-107">La `GetCountOfElementaryStreams` méthode récupère le nombre de flux élémentaires dans un programme spécifié.</span><span class="sxs-lookup"><span data-stu-id="77382-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="77382-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77382-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="77382-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77382-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77382-110">*wProgramNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77382-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77382-111">Spécifie le \_ champ du numéro de programme pour le programme, comme indiqué dans le Pat.</span><span class="sxs-lookup"><span data-stu-id="77382-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="77382-112">*pwVal* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="77382-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77382-113">Pointeur vers une variable qui reçoit le nombre de flux élémentaires dans le programme.</span><span class="sxs-lookup"><span data-stu-id="77382-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77382-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77382-114">Return value</span></span>

<span data-ttu-id="77382-115">La méthode retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77382-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="77382-116">Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="77382-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="77382-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="77382-117">Return code</span></span>                                                                          | <span data-ttu-id="77382-118">Description</span><span class="sxs-lookup"><span data-stu-id="77382-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="77382-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="77382-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="77382-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="77382-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="77382-121">Notes</span><span class="sxs-lookup"><span data-stu-id="77382-121">Remarks</span></span>

<span data-ttu-id="77382-122">Utilisez la méthode **GetRecordProgramNumber** pour obtenir le numéro du programme.</span><span class="sxs-lookup"><span data-stu-id="77382-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="77382-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77382-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77382-124">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="77382-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="77382-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="77382-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="77382-126">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="77382-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




