---
description: 'IMpeg2PsiParser :: GetRecordProgramNumber, méthode-l’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow. Il ne s’agit pas d’une API DirectShow prise en charge.'
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'IMpeg2PsiParser :: GetRecordProgramNumber, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0fd99178edaa23f2cdf32672a746f79c368b4265
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089137"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="d7654-104">IMpeg2PsiParser :: GetRecordProgramNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="d7654-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="d7654-105">L’implémentation de cette méthode est fournie sous la forme d’un exemple de code avec le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d7654-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="d7654-106">Il ne s’agit pas d’une API DirectShow prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d7654-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="d7654-107">La `GetRecordProgramNumber` méthode récupère le numéro de programme d’un programme spécifié.</span><span class="sxs-lookup"><span data-stu-id="d7654-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7654-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7654-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="d7654-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7654-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7654-110">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7654-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7654-111">Spécifie l’entrée de la PAT qui définit le programme, indexée à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="d7654-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="d7654-112">*pwVal* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7654-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7654-113">Pointeur vers une variable qui reçoit le \_ champ de numéro de programme de la Pat.</span><span class="sxs-lookup"><span data-stu-id="d7654-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7654-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7654-114">Return value</span></span>

<span data-ttu-id="d7654-115">La méthode retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7654-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="d7654-116">Les valeurs possibles sont, sans s’y limiter, les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d7654-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="d7654-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d7654-117">Return code</span></span>                                                                          | <span data-ttu-id="d7654-118">Description</span><span class="sxs-lookup"><span data-stu-id="d7654-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="d7654-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7654-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d7654-120">Réussite.</span><span class="sxs-lookup"><span data-stu-id="d7654-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d7654-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7654-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7654-122">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="d7654-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="d7654-123">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="d7654-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




