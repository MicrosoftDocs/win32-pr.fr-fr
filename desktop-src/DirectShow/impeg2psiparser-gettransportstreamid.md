---
description: L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'IMpeg2PsiParser :: GetTransportStreamId, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9615c50d8d16aa6d78e3e1b83a3ec0e356c6cb50
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519194"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a><span data-ttu-id="dad10-104">IMpeg2PsiParser :: GetTransportStreamId, méthode</span><span class="sxs-lookup"><span data-stu-id="dad10-104">IMpeg2PsiParser::GetTransportStreamId method</span></span>

<span data-ttu-id="dad10-105">L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dad10-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="dad10-106">Il ne s’agit pas d’une API DirectShow prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dad10-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="dad10-107">La `GetTransportStreamId` méthode récupère le \_ \_ champ d’ID de flux de transport à partir de Pat.</span><span class="sxs-lookup"><span data-stu-id="dad10-107">The `GetTransportStreamId` method retrieves the transport\_stream\_id field from the PAT.</span></span> <span data-ttu-id="dad10-108">Cette valeur est définie par l’utilisateur et peut être utilisée pour distinguer un flux de transport particulier d’autres flux sur le même réseau.</span><span class="sxs-lookup"><span data-stu-id="dad10-108">This value is defined by the user, and can be used to distinguish a particular transport stream from other streams on the same network.</span></span> <span data-ttu-id="dad10-109">Un flux de transport contient au plus un PAT.</span><span class="sxs-lookup"><span data-stu-id="dad10-109">A transport stream contains at most one PAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="dad10-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dad10-110">Syntax</span></span>


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a><span data-ttu-id="dad10-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dad10-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dad10-112">*pStreamId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dad10-112">*pStreamId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dad10-113">Pointeur vers une variable qui reçoit le \_ champ ID du flux de transport \_ .</span><span class="sxs-lookup"><span data-stu-id="dad10-113">Pointer to a variable that receives the transport\_stream\_id field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dad10-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dad10-114">Return value</span></span>

<span data-ttu-id="dad10-115">La méthode retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dad10-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="dad10-116">Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dad10-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="dad10-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dad10-117">Return code</span></span>                                                                          | <span data-ttu-id="dad10-118">Description</span><span class="sxs-lookup"><span data-stu-id="dad10-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="dad10-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dad10-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dad10-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="dad10-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="dad10-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dad10-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad10-122">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="dad10-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="dad10-123">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="dad10-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




