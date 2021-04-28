---
description: 'IMpeg2PsiParser :: GetCountOfElementaryStreams, méthode-l’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.'
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
ms.openlocfilehash: fc81c0a66751751a73a3895fd31fe8651aee8caf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089157"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="983ee-104">IMpeg2PsiParser :: GetCountOfElementaryStreams, méthode</span><span class="sxs-lookup"><span data-stu-id="983ee-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="983ee-105">L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="983ee-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="983ee-106">Il ne s’agit pas d’une API DirectShow prise en charge.</span><span class="sxs-lookup"><span data-stu-id="983ee-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="983ee-107">La `GetCountOfElementaryStreams` méthode récupère le nombre de flux élémentaires dans un programme spécifié.</span><span class="sxs-lookup"><span data-stu-id="983ee-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="983ee-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="983ee-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="983ee-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="983ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="983ee-110">*wProgramNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="983ee-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="983ee-111">Spécifie le \_ champ du numéro de programme pour le programme, comme indiqué dans le Pat.</span><span class="sxs-lookup"><span data-stu-id="983ee-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="983ee-112">*pwVal* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="983ee-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="983ee-113">Pointeur vers une variable qui reçoit le nombre de flux élémentaires dans le programme.</span><span class="sxs-lookup"><span data-stu-id="983ee-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="983ee-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="983ee-114">Return value</span></span>

<span data-ttu-id="983ee-115">La méthode retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="983ee-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="983ee-116">Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="983ee-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="983ee-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="983ee-117">Return code</span></span>                                                                          | <span data-ttu-id="983ee-118">Description</span><span class="sxs-lookup"><span data-stu-id="983ee-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="983ee-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="983ee-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="983ee-120">Réussite.</span><span class="sxs-lookup"><span data-stu-id="983ee-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="983ee-121">Notes </span><span class="sxs-lookup"><span data-stu-id="983ee-121">Remarks</span></span>

<span data-ttu-id="983ee-122">Utilisez la méthode **GetRecordProgramNumber** pour obtenir le numéro du programme.</span><span class="sxs-lookup"><span data-stu-id="983ee-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="983ee-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="983ee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983ee-124">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="983ee-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="983ee-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="983ee-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="983ee-126">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="983ee-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




