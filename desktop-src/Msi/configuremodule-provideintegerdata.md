---
description: La méthode ProvideIntegerData de l’objet ConfigureModule est appelée par Mergemod.dll pour récupérer des données de type entier à partir de l’outil client.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Méthode ConfigureModule. ProvideIntegerData (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526444"
---
# <a name="configuremoduleprovideintegerdata-method"></a><span data-ttu-id="1dde7-103">Méthode ConfigureModule. ProvideIntegerData</span><span class="sxs-lookup"><span data-stu-id="1dde7-103">ConfigureModule.ProvideIntegerData method</span></span>

<span data-ttu-id="1dde7-104">La méthode **ProvideIntegerData** de l' [**objet ConfigureModule**](configuremodule-object.md) est appelée par Mergemod.dll pour récupérer des données de type entier à partir de l’outil client.</span><span class="sxs-lookup"><span data-stu-id="1dde7-104">The **ProvideIntegerData** method of the [**ConfigureModule object**](configuremodule-object.md) is called by Mergemod.dll to retrieve integer data from the client tool.</span></span>

<span data-ttu-id="1dde7-105">Mergemod.dll fournit le *nom* à partir de l’entrée correspondante dans la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1dde7-105">Mergemod.dll provides the *Name* from the corresponding entry in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="1dde7-106">L’outil doit retourner S \_ OK et fournir l’entier de personnalisation approprié dans *ConfigData*.</span><span class="sxs-lookup"><span data-stu-id="1dde7-106">The tool should return S\_OK and provide the appropriate customization integer in *ConfigData*.</span></span>

<span data-ttu-id="1dde7-107">Si l’outil ne fournit pas de données de configuration pour cette valeur de *nom* , la fonction doit retourner S \_ false.</span><span class="sxs-lookup"><span data-stu-id="1dde7-107">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="1dde7-108">Dans ce cas Mergemod.dll ignore la valeur de l’argument *ConfigData* et utilise la valeur par défaut de la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1dde7-108">In this case Mergemod.dll ignores the value of the *ConfigData* argument and uses the Default value from the ModuleConfiguration table.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dde7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1dde7-109">Syntax</span></span>


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="1dde7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1dde7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dde7-111">*Nom*</span><span class="sxs-lookup"><span data-stu-id="1dde7-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="1dde7-112">Nom de l’élément pour lequel les données sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="1dde7-112">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="1dde7-113">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="1dde7-113">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="1dde7-114">Pointeur vers le texte de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="1dde7-114">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dde7-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1dde7-115">Return value</span></span>

<span data-ttu-id="1dde7-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1dde7-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dde7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1dde7-117">Remarks</span></span>

<span data-ttu-id="1dde7-118">Le client peut être appelé plusieurs fois pour chaque enregistrement de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1dde7-118">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="1dde7-119">Notez que Mergemod.dll n’effectue jamais plusieurs appels au client pour la même valeur « Name ».</span><span class="sxs-lookup"><span data-stu-id="1dde7-119">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="1dde7-120">Si aucun enregistrement de la table ModuleSubstitution n’utilise la propriété, une entrée de la table ModuleConfiguration n’entraîne aucun appel au client.</span><span class="sxs-lookup"><span data-stu-id="1dde7-120">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="1dde7-121">C++</span><span class="sxs-lookup"><span data-stu-id="1dde7-121">C++</span></span>

<span data-ttu-id="1dde7-122">Consultez [**fonction ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span><span class="sxs-lookup"><span data-stu-id="1dde7-122">See [**ProvideIntegerData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="1dde7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1dde7-123">Requirements</span></span>



| <span data-ttu-id="1dde7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1dde7-124">Requirement</span></span> | <span data-ttu-id="1dde7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1dde7-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dde7-126">Version</span><span class="sxs-lookup"><span data-stu-id="1dde7-126">Version</span></span><br/> | <span data-ttu-id="1dde7-127">Mergemod.dll 2,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1dde7-127">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="1dde7-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="1dde7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1dde7-129"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dde7-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="1dde7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1dde7-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="1dde7-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dde7-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




