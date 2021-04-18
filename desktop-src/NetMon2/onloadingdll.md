---
description: Charge la DLL du moniteur.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: OnLoadingDLL, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536124"
---
# <a name="onloadingdll-function"></a><span data-ttu-id="ec3e2-103">OnLoadingDLL fonction)</span><span class="sxs-lookup"><span data-stu-id="ec3e2-103">OnLoadingDLL function</span></span>

<span data-ttu-id="ec3e2-104">La fonction **OnLoadingDLL** charge la dll de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-104">The **OnLoadingDLL** function loads the monitor DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec3e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec3e2-105">Syntax</span></span>


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a><span data-ttu-id="ec3e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec3e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec3e2-107">*hFilterBlob* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ec3e2-107">*hFilterBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3e2-108">Objet BLOB utilisé par le MCSVC pour correspondre à une analyse avec des cartes réseau disponibles.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-108">A BLOB that the MCSVC uses to match a monitor with available NICs.</span></span> <span data-ttu-id="ec3e2-109">Ce paramètre contient toujours une demande pour une interface [IRTC](irtc.md) . la plupart des analyses n’ont donc pas besoin d’ajouter d’entrées à l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-109">This parameter always contains a request for an [IRTC](irtc.md) interface, so most monitors do not need to add any entries to the BLOB.</span></span> <span data-ttu-id="ec3e2-110">Toutefois, une analyse personnalisée peut ajouter des critères de filtre supplémentaires (par exemple, si le type MAC doit être Ethernet).</span><span class="sxs-lookup"><span data-stu-id="ec3e2-110">However, a custom monitor can add additional filter criteria (for example, that the MAC type must be Ethernet).</span></span>

</dd> <dt>

<span data-ttu-id="ec3e2-111">*pCreateFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec3e2-111">*pCreateFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3e2-112">Indicateurs qui indiquent comment le MCSVC contrôle la création d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-112">The flags that indicate how the MCSVC controls the creation of a monitor.</span></span> <span data-ttu-id="ec3e2-113">Ce paramètre doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ec3e2-113">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="ec3e2-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec3e2-114">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="ec3e2-115">Signification</span><span class="sxs-lookup"><span data-stu-id="ec3e2-115">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <span data-ttu-id="ec3e2-116"><dt>**MCS \_ créer \_ un \_ par \_ carte réseau**</dt></span><span class="sxs-lookup"><span data-stu-id="ec3e2-116"><dt>**MCS\_CREATE\_ONE\_PER\_NETCARD**</dt></span></span> </dl>          | <span data-ttu-id="ec3e2-117">Le MCSVC garantit qu’une seule instance de ce moniteur existe pour chaque carte réseau.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-117">The MCSVC ensures that only one instance of this monitor exists for each NIC.</span></span> <span data-ttu-id="ec3e2-118">Une deuxième instance peut être créée uniquement si la première est détruite.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-118">A second instance can be created only if the first one is destroyed.</span></span><br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <span data-ttu-id="ec3e2-119"><dt>**MCS- \_ créer \_ \_ des configurations par \_ défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="ec3e2-119"><dt>**MCS\_CREATE\_CONFIGS\_BY\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="ec3e2-120">Si le moniteur a une configuration interne par défaut, MCSVC ne demande pas à l’utilisateur de configurer le moniteur avant la création de l’instance.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-120">If the monitor has a default internal configuration, the MCSVC does not require the user to configure the monitor before the instance is created.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="ec3e2-121">*ppDefaultName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ec3e2-121">*ppDefaultName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3e2-122">Pointeur vers un pointeur vers l’adresse du nom par défaut de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-122">A pointer to a pointer to the address of the default name of the monitor.</span></span> <span data-ttu-id="ec3e2-123">Le MCSVC utilise le nom par défaut lors de la création d’instances de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-123">The MCSVC uses the default name when creating instances of the monitor.</span></span>

<span data-ttu-id="ec3e2-124">Par exemple, si le nom par défaut retourné est « moniteur de routeur », la première instance de l’analyse serait « moniteur de routeur 1 », la deuxième « RouterMonitor2 », et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-124">For example, if the returned default name is "Router Monitor", the first monitor instance would be "Router Monitor 1", the second would be "RouterMonitor2, and so on.</span></span> <span data-ttu-id="ec3e2-125">Si la **valeur null** est retournée, MCSVC utilise le nom de la dll.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-125">If **NULL** is returned, the MCSVC uses the name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="ec3e2-126">*ppDescription* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ec3e2-126">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3e2-127">Pointeur vers un pointeur vers l’adresse de la description de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-127">A pointer to a pointer to the address of the description of the monitor.</span></span> <span data-ttu-id="ec3e2-128">La description est transmise à l’outil de contrôle de l’analyse, qui utilise la description pour indiquer à l’utilisateur que le moniteur existe.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-128">The description is passed to the Monitor Control Tool, which uses the description to indicate to the user that the monitor exists.</span></span> <span data-ttu-id="ec3e2-129">Ce paramètre peut retourner la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-129">This parameter can return **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ec3e2-130">*ppDefaultScript* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ec3e2-130">*ppDefaultScript* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3e2-131">Pointeur vers un pointeur vers l’adresse du script de formulaire HTML par défaut utilisé pour configurer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-131">A pointer to a pointer to the address of the default HTML Form script used to configure the monitor.</span></span> <span data-ttu-id="ec3e2-132">Bien que les instances du moniteur puissent modifier leur propre script, la plupart des analyses chargent simplement leur script une seule fois, à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-132">Although the instances of the monitor can alter their own script, most monitors simply load their script once, from a file.</span></span> <span data-ttu-id="ec3e2-133">La valeur de *ppDefaultScript* peut être **null**. Toutefois, soit le moniteur ne peut pas être configuré en externe, soit il doit fournir un script ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-133">The value of *ppDefaultScript* can be **NULL**; however, then either the monitor cannot be externally configured, or it must supply a script later.</span></span> <span data-ttu-id="ec3e2-134">Il est plus efficace de fournir un script par défaut ici.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-134">It is more efficient to supply a default script here.</span></span>

</dd> <dt>

<span data-ttu-id="ec3e2-135">*ppDefaultConfig* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ec3e2-135">*ppDefaultConfig* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3e2-136">Adresse de la chaîne par défaut utilisée pour configurer l’analyse lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-136">The address of the default string used to configure the monitor when it is created.</span></span> <span data-ttu-id="ec3e2-137">Ce paramètre peut avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-137">This parameter can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec3e2-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec3e2-138">Return value</span></span>

<span data-ttu-id="ec3e2-139">Si la fonction réussit, la valeur de retour est S OK, ce \_ qui est identique à l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-139">If the function is successful, the return value is S\_OK; which is the same as NOERROR.</span></span>

<span data-ttu-id="ec3e2-140">Si la fonction échoue, le MCSVC omet le moniteur spécifié dans toutes ses listes ; après, aucune analyse de ce type ne peut être créée.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-140">If the function is unsuccessful, the MCSVC omits the specified monitor from all its lists; after, no monitor of this type can be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec3e2-141">Notes</span><span class="sxs-lookup"><span data-stu-id="ec3e2-141">Remarks</span></span>

<span data-ttu-id="ec3e2-142">La fonction **OnLoadingDLL** est appelée une fois par MCSVC, lors du premier chargement de la dll.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-142">The **OnLoadingDLL** function is called once by the MCSVC, when it first loads the DLL.</span></span> <span data-ttu-id="ec3e2-143">La DLL fournit ensuite les valeurs par défaut qui seront utilisées par le MCSVC lors de la création d’une instance d’analyse.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-143">The DLL then provides the default values that will be used by the MCSVC when creating an instance of a monitor.</span></span>

<span data-ttu-id="ec3e2-144">L’analyse doit allouer toute la mémoire nécessaire pour les chaînes retournées à MCSVC.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-144">The monitor must allocate all the necessary memory for the strings returned to the MCSVC.</span></span> <span data-ttu-id="ec3e2-145">Au retour, le MCSVC crée des copies de toutes les chaînes et ne tente pas de libérer les chaînes retournées.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-145">On return, the MCSVC makes copies of all the strings and will not attempt to free the returned strings.</span></span>

<span data-ttu-id="ec3e2-146">Le moniteur doit utiliser les fonctions d’assistance de BLOB pour modifier l’objet BLOB de filtre.</span><span class="sxs-lookup"><span data-stu-id="ec3e2-146">The monitor should use BLOB helper functions to alter the filter BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec3e2-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec3e2-147">Requirements</span></span>



| <span data-ttu-id="ec3e2-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec3e2-148">Requirement</span></span> | <span data-ttu-id="ec3e2-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec3e2-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3e2-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec3e2-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ec3e2-151">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec3e2-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ec3e2-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec3e2-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ec3e2-153">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec3e2-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ec3e2-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec3e2-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec3e2-155"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec3e2-155"><dt>Netmon.h</dt></span></span> </dl> |



 

 




