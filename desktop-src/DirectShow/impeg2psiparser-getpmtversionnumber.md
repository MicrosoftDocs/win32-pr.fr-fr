---
description: L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'IMpeg2PsiParser :: GetPmtVersionNumber, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515738"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="dadd1-104">IMpeg2PsiParser :: GetPmtVersionNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="dadd1-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="dadd1-105">L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dadd1-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="dadd1-106">Il ne s’agit pas d’une API DirectShow prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dadd1-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="dadd1-107">La `GetPmtVersionNumber` méthode récupère le champ du \_ numéro de version à partir d’un PMT spécifié.</span><span class="sxs-lookup"><span data-stu-id="dadd1-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="dadd1-108">Le numéro de version est incrémenté chaque fois que la définition du programme change.</span><span class="sxs-lookup"><span data-stu-id="dadd1-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="dadd1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dadd1-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="dadd1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dadd1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dadd1-111">*wProgramNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dadd1-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dadd1-112">Spécifie le \_ champ du numéro de programme du programme, comme indiqué dans le Pat.</span><span class="sxs-lookup"><span data-stu-id="dadd1-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="dadd1-113">*pPmtVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dadd1-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dadd1-114">Pointeur vers une variable qui reçoit le champ du numéro de version \_ .</span><span class="sxs-lookup"><span data-stu-id="dadd1-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dadd1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dadd1-115">Return value</span></span>

<span data-ttu-id="dadd1-116">La méthode retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dadd1-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="dadd1-117">Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dadd1-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="dadd1-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dadd1-118">Return code</span></span>                                                                          | <span data-ttu-id="dadd1-119">Description</span><span class="sxs-lookup"><span data-stu-id="dadd1-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="dadd1-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dadd1-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dadd1-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="dadd1-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dadd1-122">Notes</span><span class="sxs-lookup"><span data-stu-id="dadd1-122">Remarks</span></span>

<span data-ttu-id="dadd1-123">Utilisez la méthode **GetRecordProgramNumber** pour obtenir le numéro du programme.</span><span class="sxs-lookup"><span data-stu-id="dadd1-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="dadd1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dadd1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dadd1-125">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="dadd1-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="dadd1-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="dadd1-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="dadd1-127">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="dadd1-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




