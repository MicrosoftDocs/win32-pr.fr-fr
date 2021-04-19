---
description: La méthode ProvideTextData est appelée par Mergemod.dll pour récupérer des données de texte à partir de l’outil client. Mergemod.dll fournit le nom à partir de l’entrée correspondante dans la table ModuleConfiguration.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Méthode ConfigureModule. ProvideTextData (Mergemod. h)
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
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530006"
---
# <a name="configuremoduleprovidetextdata-method"></a><span data-ttu-id="5be06-104">Méthode ConfigureModule. ProvideTextData</span><span class="sxs-lookup"><span data-stu-id="5be06-104">ConfigureModule.ProvideTextData method</span></span>

<span data-ttu-id="5be06-105">La méthode **ProvideTextData** est appelée par Mergemod.dll pour récupérer des données de texte à partir de l’outil client.</span><span class="sxs-lookup"><span data-stu-id="5be06-105">The **ProvideTextData** method is called by Mergemod.dll to retrieve text data from the client tool.</span></span> <span data-ttu-id="5be06-106">Mergemod.dll fournit le *nom* à partir de l’entrée correspondante dans la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5be06-106">Mergemod.dll provides the *Name* from the corresponding entry in the ModuleConfiguration table.</span></span>

<span data-ttu-id="5be06-107">L’outil doit retourner S \_ OK et fournir le texte de personnalisation approprié dans ConfigData.</span><span class="sxs-lookup"><span data-stu-id="5be06-107">The tool should return S\_OK and provide the appropriate customization text in ConfigData.</span></span> <span data-ttu-id="5be06-108">L’outil client est chargé d’allouer les données, mais Mergemod.dllest responsable de la libération de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="5be06-108">The client tool is responsible for allocating the data, but Mergemod.dllis responsible for releasing the memory.</span></span> <span data-ttu-id="5be06-109">Cet argument doit être un objet **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="5be06-109">This argument MUST be a **BSTR** object.</span></span> <span data-ttu-id="5be06-110">**LPCWSTR** n’est pas accepté.</span><span class="sxs-lookup"><span data-stu-id="5be06-110">**LPCWSTR** is NOT accepted.</span></span>

<span data-ttu-id="5be06-111">Si l’outil ne fournit pas de données de configuration pour cette valeur de *nom* , la fonction doit retourner S \_ false.</span><span class="sxs-lookup"><span data-stu-id="5be06-111">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="5be06-112">Dans ce cas Mergemod.dll ignore la valeur de l’argument ConfigData et utilise la valeur par défaut de la table ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5be06-112">In this case Mergemod.dll ignores the value of the ConfigData argument and uses the Default value from the ModuleConfiguration table.</span></span>

<span data-ttu-id="5be06-113">Tout code de retour autre que S \_ OK ou s \_ false entraîne la journalisation d’une erreur (si un journal est ouvert) et entraîne l’échec de la fusion.</span><span class="sxs-lookup"><span data-stu-id="5be06-113">Any return code other than S\_OK or S\_FALSE will cause an error to be logged (if a log is open) and will result in the merge failing.</span></span>

<span data-ttu-id="5be06-114">Étant donné que cette fonction suit la convention **BSTR** standard, NULL est équivalent à la chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="5be06-114">Because this function follows standard **BSTR** convention, null is equivalent to the empty string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5be06-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5be06-115">Syntax</span></span>


```JScript
ConfigureModule.ProvideTextData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="5be06-116">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5be06-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5be06-117">*Nom*</span><span class="sxs-lookup"><span data-stu-id="5be06-117">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="5be06-118">Nom de l’élément pour lequel les données sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="5be06-118">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="5be06-119">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="5be06-119">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="5be06-120">Pointeur vers le texte de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="5be06-120">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5be06-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5be06-121">Return value</span></span>

<span data-ttu-id="5be06-122">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5be06-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5be06-123">Notes</span><span class="sxs-lookup"><span data-stu-id="5be06-123">Remarks</span></span>

<span data-ttu-id="5be06-124">Le client peut être appelé plusieurs fois pour chaque enregistrement de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="5be06-124">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="5be06-125">Notez que Mergemod.dll n’effectue jamais plusieurs appels au client pour la même valeur « Name ».</span><span class="sxs-lookup"><span data-stu-id="5be06-125">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="5be06-126">Si aucun enregistrement de la table ModuleSubstitution n’utilise la propriété, une entrée de la table ModuleConfiguration n’entraîne aucun appel au client.</span><span class="sxs-lookup"><span data-stu-id="5be06-126">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="5be06-127">C++</span><span class="sxs-lookup"><span data-stu-id="5be06-127">C++</span></span>

<span data-ttu-id="5be06-128">Consultez [**fonction ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span><span class="sxs-lookup"><span data-stu-id="5be06-128">See [**ProvideTextData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="5be06-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5be06-129">Requirements</span></span>



| <span data-ttu-id="5be06-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5be06-130">Requirement</span></span> | <span data-ttu-id="5be06-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5be06-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5be06-132">Version</span><span class="sxs-lookup"><span data-stu-id="5be06-132">Version</span></span><br/> | <span data-ttu-id="5be06-133">Mergemod.dll 2,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5be06-133">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5be06-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="5be06-134">Header</span></span><br/>  | <dl> <span data-ttu-id="5be06-135"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="5be06-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5be06-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5be06-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="5be06-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5be06-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




