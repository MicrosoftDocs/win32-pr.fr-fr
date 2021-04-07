---
description: Lors de l’installation d’un fournisseur de réseau, votre application doit créer les clés de Registre et les valeurs décrites dans cette rubrique.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Clés de registre d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952216"
---
# <a name="authentication-registry-keys"></a><span data-ttu-id="e1bf9-103">Clés de registre d’authentification</span><span class="sxs-lookup"><span data-stu-id="e1bf9-103">Authentication Registry Keys</span></span>

<span data-ttu-id="e1bf9-104">Lors de l’installation d’un fournisseur de réseau, votre application doit créer les clés de Registre et les valeurs décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-104">When it installs a network provider, your application should create the registry keys and values described in this topic.</span></span> <span data-ttu-id="e1bf9-105">Ces clés et ces valeurs fournissent des informations à l’MPR sur les fournisseurs de réseau installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-105">These keys and values provide information to the MPR about the network providers installed on the system.</span></span> <span data-ttu-id="e1bf9-106">Le service MPR vérifie ces clés lorsqu’il démarre et charge les dll du fournisseur réseau qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-106">The MPR checks these keys when it starts and loads the network provider DLLs that it finds.</span></span>

<span data-ttu-id="e1bf9-107">Avant de créer un ensemble de clés pour stocker des informations sur votre fournisseur réseau, vous devez ajouter le nom de votre fournisseur de réseau à la clé de **commande** .</span><span class="sxs-lookup"><span data-stu-id="e1bf9-107">Before you create a set of keys to hold information about your network provider, you should add the name of your network provider to the **order** key.</span></span> <span data-ttu-id="e1bf9-108">Cette clé est une sous-clé de la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="e1bf9-108">This key is a subkey of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

<span data-ttu-id="e1bf9-109">La clé de **commande** contient une valeur unique, **ProviderOrder**, qui répertorie les fournisseurs installés et spécifie l’ordre dans lequel ils doivent être essayés pendant les opérations qui traversent les fournisseurs jusqu’à ce qu’un fournisseur acceptant soit trouvé.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-109">The **order** key contains a single value, **ProviderOrder**, which lists the installed providers and specifies the order in which they should be tried during operations that cycle through providers until an accepting provider is found.</span></span>

<span data-ttu-id="e1bf9-110">La valeur **ProviderOrder** contient une liste de noms de clés séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-110">The **ProviderOrder** value contains a comma-separated list of key names.</span></span> <span data-ttu-id="e1bf9-111">Chaque nom de clé dans **ProviderOrder** identifie un fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-111">Each key name in **ProviderOrder** identifies a network provider.</span></span> <span data-ttu-id="e1bf9-112">Lorsque MPR parcourt les fournisseurs, il les appelle dans l’ordre dans lequel ils apparaissent dans cette liste.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-112">When MPR cycles through the providers, it calls them in the order in which they appear in this list.</span></span>

<span data-ttu-id="e1bf9-113">Le nom de fournisseur défini dans **ProviderOrder** doit également être utilisé comme nom de la clé de Registre qui contient des informations sur ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-113">The provider name set in **ProviderOrder** should also be used as the name of the registry key that contains information about that provider.</span></span> <span data-ttu-id="e1bf9-114">Les clés de Registre spécifiques au fournisseur sont créées en tant que sous-clés de la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="e1bf9-114">The provider-specific registry keys are created as subkeys of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="e1bf9-115">En d’autres termes, les noms de fournisseurs spécifiés dans **ProviderOrder** sont le chemin d’accès au registre des clés spécifiques au fournisseur de réseau, par rapport au chemin d’accès suivant :</span><span class="sxs-lookup"><span data-stu-id="e1bf9-115">In other words, the provider names specified in **ProviderOrder** are the path to the registry of the network provider-specific keys, relative to the following path:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="e1bf9-116">Lorsque votre service de fournisseur de réseau est installé, l’application d’installation doit ajouter une clé comme suit :</span><span class="sxs-lookup"><span data-stu-id="e1bf9-116">When your network provider service is installed, the installation application should add a key as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

<span data-ttu-id="e1bf9-117">Où *providerName* est le nom du fournisseur réseau, tel que spécifié dans la valeur **ProviderOrder** de la clé de **commande** .</span><span class="sxs-lookup"><span data-stu-id="e1bf9-117">Where *ProviderName* is the name of the network provider as specified in the **ProviderOrder** value of the **order** key.</span></span> <span data-ttu-id="e1bf9-118">La valeur de **groupe** sous la clé *providerName* doit être définie sur « NetworkProvider ».</span><span class="sxs-lookup"><span data-stu-id="e1bf9-118">The **Group** value under the *ProviderName* key should be set to "NetworkProvider".</span></span> <span data-ttu-id="e1bf9-119">Cela identifie le service comme étant dans le groupe de fournisseurs de réseau.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-119">This identifies the service as being in the network provider group.</span></span>

<span data-ttu-id="e1bf9-120">Vous devez également créer une sous-clé de *providerName*, **NetworkProvider**.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-120">You must also create a subkey of *ProviderName*, **networkprovider**.</span></span> <span data-ttu-id="e1bf9-121">Cette clé contient les valeurs suivantes qui décrivent le fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-121">This key contains the following values that describe the network provider.</span></span>



| <span data-ttu-id="e1bf9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1bf9-122">Value</span></span>                       | <span data-ttu-id="e1bf9-123">Description</span><span class="sxs-lookup"><span data-stu-id="e1bf9-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1bf9-124">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e1bf9-124">**Name**</span></span><br/>         | <span data-ttu-id="e1bf9-125">Contient le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-125">Contains the name of the provider.</span></span> <span data-ttu-id="e1bf9-126">Ce nom est affiché pour l’utilisateur en tant que nom du réseau dans les boîtes de dialogue de navigation et doit correspondre au champ **lpProvider** renvoyé dans les structures de [**ressources**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) réseau.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-126">This name is displayed to the user as the name of the network in the browse dialog boxes and should match the **lpProvider** field returned in [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures.</span></span> <span data-ttu-id="e1bf9-127">Ce nom doit être une variante du nom du produit, de préférence avec une certaine indication de la société, afin qu’elle soit claire et unique.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-127">This name should be some variation of the product name, preferably with some indication of the company as well, so that it is clear and unique.</span></span> <span data-ttu-id="e1bf9-128">« MS-LanMan », par exemple, est un bon nom, tandis que « The net » est un mauvais choix.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-128">"MS-LanMan" for example is a good name, whereas "The Net" would be a poor choice.</span></span><br/> |
| <span data-ttu-id="e1bf9-129">**ProviderPath**</span><span class="sxs-lookup"><span data-stu-id="e1bf9-129">**ProviderPath**</span></span><br/> | <span data-ttu-id="e1bf9-130">Contient le chemin d’accès complet de la DLL qui implémente le fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-130">Contains the full path of the DLL that implements the network provider.</span></span> <span data-ttu-id="e1bf9-131">MPR appelle [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) sur ce chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-131">MPR calls [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) on this path.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="e1bf9-132">Les valeurs suivantes sont utilisées uniquement par les fournisseurs de réseau qui prennent en charge les fonctions de gestion des informations d’identification, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) et [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span><span class="sxs-lookup"><span data-stu-id="e1bf9-132">The following values are used only by network providers that support the credential management functions, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span></span>



| <span data-ttu-id="e1bf9-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1bf9-133">Value</span></span>                              | <span data-ttu-id="e1bf9-134">Description</span><span class="sxs-lookup"><span data-stu-id="e1bf9-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1bf9-135">**Classe**</span><span class="sxs-lookup"><span data-stu-id="e1bf9-135">**Class**</span></span><br/>               | <span data-ttu-id="e1bf9-136">**Valeur DWORD** qui identifie la classe, ou le type, de la fonctionnalité de fournisseur prise en charge par ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-136">A **DWORD** that identifies the class, or type, of provider functionality that this provider supports.</span></span> <span data-ttu-id="e1bf9-137">Les valeurs peuvent être jointes par l’opérateur **or** , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-137">Values may be joined by the **OR** operator when appropriate.</span></span> <span data-ttu-id="e1bf9-138">Les valeurs valides sont : WN \_ Network, classe, la classe \_ \_ Credential WN, la \_ \_ \_ classe AUTHENT principale WN et la \_ \_ classe de service WN \_ .</span><span class="sxs-lookup"><span data-stu-id="e1bf9-138">Valid values for this are WN\_NETWORK\_CLASS, WN\_CREDENTIAL\_CLASS, WN\_PRIMARY\_AUTHENT\_CLASS, and WN\_SERVICE\_CLASS.</span></span><br/> <span data-ttu-id="e1bf9-139">Bien qu’un fournisseur puisse prendre en charge la fonctionnalité d’authentificateur principal, un autre moyen sera utilisé pour déterminer quel authentificateur est principal.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-139">Although a provider may support primary authenticator functionality, another means will be used to determine which authenticator is primary.</span></span><br/> <span data-ttu-id="e1bf9-140">**Windows XP/2000 :** Le changement d’authentificateurs principal n’est pas pris en charge. cette valeur est donc ignorée.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-140">**Windows XP/2000:** Switching primary authenticators is not supported, so this value is ignored.</span></span> <br/> |
| <span data-ttu-id="e1bf9-141">**AuthentProviderPath**</span><span class="sxs-lookup"><span data-stu-id="e1bf9-141">**AuthentProviderPath**</span></span><br/> | <span data-ttu-id="e1bf9-142">Il s’agit du nom de fichier complet de la DLL qui exporte les fonctions de gestion des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-142">This is the fully qualified file name for the DLL that exports the Credential Management Functions.</span></span> <span data-ttu-id="e1bf9-143">Cette valeur est utile (mais pas obligatoire) uniquement lorsque le fournisseur est identifié comme étant une classe d’informations d’identification \_ ou un \_ fournisseur de classe AUTHENT primaire \_ .</span><span class="sxs-lookup"><span data-stu-id="e1bf9-143">This value is useful (but not required) only when the provider is identified as being a CREDENTIAL\_CLASS or PRIMARY\_AUTHENT\_CLASS provider.</span></span> <span data-ttu-id="e1bf9-144">Si cette valeur n’est pas présente pour un fournisseur de cette classe, les fonctions de gestion des informations d’identification doivent être exportées à partir de la DLL identifiée par la valeur ProviderPath.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-144">If this value is not present for a provider of this class, the credential management functions are expected to be exported from the DLL identified by the ProviderPath value.</span></span> <span data-ttu-id="e1bf9-145">Cette valeur est utilisée uniquement s’il est souhaitable d’empaqueter les fonctions réseau et les fonctions du gestionnaire d’informations d’identification dans des dll distinctes.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-145">This value is used only if it is desirable to package the network functions and the credential manager functions in separate DLLs.</span></span><br/>  |



 

<span data-ttu-id="e1bf9-146">Outre les valeurs utilisées pour enregistrer les fournisseurs de réseau et les gestionnaires d’informations d’identification, vous pouvez ajouter une valeur au registre pour inscrire une DLL afin de recevoir des notifications de connexion.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-146">In addition to the values used to register network providers and credential managers, you can add a value to the registry to register a DLL to receive connection notifications.</span></span> <span data-ttu-id="e1bf9-147">Pour ce faire, créez une \_ valeur de \_ la valeur SZ reg Expand sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="e1bf9-147">To do so, create a REG\_EXPAND\_SZ value under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

<span data-ttu-id="e1bf9-148">Cette valeur doit spécifier le chemin d’accès à une DLL qui implémente l' [API de notification de connexion](connection-notification-api.md).</span><span class="sxs-lookup"><span data-stu-id="e1bf9-148">This value should specify the path to a DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span> <span data-ttu-id="e1bf9-149">Le nom de cette valeur peut être tout ce que vous voulez, à condition qu’il n’entre pas en conflit avec les noms de valeurs préexistants.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-149">The name of this value can be anything you want, as long as it does not conflict with preexisting value names.</span></span>

## <a name="example"></a><span data-ttu-id="e1bf9-150">Exemple</span><span class="sxs-lookup"><span data-stu-id="e1bf9-150">Example</span></span>

<span data-ttu-id="e1bf9-151">L’exemple suivant montre les clés de Registre pour un système sur lequel deux fournisseurs de réseau sont installés : LanmanWorkStation et AnotherNetSvc.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-151">The following example shows the registry keys for a system that has two network providers installed: LanmanWorkStation and AnotherNetSvc.</span></span> <span data-ttu-id="e1bf9-152">AnotherNetSvc est également un gestionnaire d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-152">AnotherNetSvc is also a credential manager.</span></span> <span data-ttu-id="e1bf9-153">Dans l’exemple, les noms de clé sont en gras et les noms de valeur sont en italique.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-153">In the example, key names are bold and value names are italic.</span></span>

<span data-ttu-id="e1bf9-154">**HKEY \_ \_** \\  \\  \\  \\  \\ **Ordre** NetworkProvider du contrôle CurrentControlSet du système de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="e1bf9-154">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**order**</span></span>

<span data-ttu-id="e1bf9-155">*ProviderOrder* = "LanmanWorkStation, AnotherNetSvc"</span><span class="sxs-lookup"><span data-stu-id="e1bf9-155">*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"</span></span>

<span data-ttu-id="e1bf9-156">**HKEY \_ \_** \\  \\  \\  \\  \\ **Notifications** de contrôles CurrentControlSet du système d’ordinateur local NetworkProvider</span><span class="sxs-lookup"><span data-stu-id="e1bf9-156">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="e1bf9-157">*MyNotifyApp* = "c : \\ Connect \\connect.dll"</span><span class="sxs-lookup"><span data-stu-id="e1bf9-157">*MyNotifyApp* = "c:\\connect\\connect.dll"</span></span>

<span data-ttu-id="e1bf9-158">**HKEY \_ \_** \\  \\  \\ **Services** de CurrentControlSet de système \\  d’ordinateur local LanmanWorkStation</span><span class="sxs-lookup"><span data-stu-id="e1bf9-158">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**</span></span>\\

<span data-ttu-id="e1bf9-159">*Groupe* = « NetworkProvider »</span><span class="sxs-lookup"><span data-stu-id="e1bf9-159">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="e1bf9-160">**HKEY \_ Services d' \_ ordinateur local** \\ **système** de \\ **CurrentControlSet** \\  \\  \\ **NetworkProvider** LanmanWorkStation</span><span class="sxs-lookup"><span data-stu-id="e1bf9-160">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**\\**NetworkProvider**</span></span>

<span data-ttu-id="e1bf9-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span><span class="sxs-lookup"><span data-stu-id="e1bf9-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span></span>

<span data-ttu-id="e1bf9-162">*Class* = 0x00000001 ( \_ classe réseau WN \_ )</span><span class="sxs-lookup"><span data-stu-id="e1bf9-162">*Class* = 0x00000001 (WN\_NETWORK\_CLASS)</span></span>

<span data-ttu-id="e1bf9-163">**HKEY \_ \_** \\  \\  \\ **Services** de CurrentControlSet de système \\  d’ordinateur local AnotherNetSvc</span><span class="sxs-lookup"><span data-stu-id="e1bf9-163">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**</span></span>\\

<span data-ttu-id="e1bf9-164">*Groupe* = « NetworkProvider »</span><span class="sxs-lookup"><span data-stu-id="e1bf9-164">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="e1bf9-165">**HKEY \_ \_** Services de CurrentControlSet de système d’ordinateur local \\  \\  \\  \\ **AnotherNetSvc** \\ **NetworkProvider**</span><span class="sxs-lookup"><span data-stu-id="e1bf9-165">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**\\**NetworkProvider**</span></span>

<span data-ttu-id="e1bf9-166">*Name* = "un autre réseau"*ProviderPath* = "c : \\ un autre \\anet.dll"</span><span class="sxs-lookup"><span data-stu-id="e1bf9-166">*Name* = "Another Network"*ProviderPath* = "c:\\another\\anet.dll"</span></span>

<span data-ttu-id="e1bf9-167">*Class* = 0x00000003 (classe \_ \_ \| \_ d’informations d’identification \_ de la classe de réseau Wn)</span><span class="sxs-lookup"><span data-stu-id="e1bf9-167">*Class* = 0x00000003 (WN\_NETWORK\_CLASS \| WN\_CREDENTIAL\_CLASS)</span></span>

<span data-ttu-id="e1bf9-168">*AuthentProviderPath* = "c : \\ autre \\anetCM.dll"</span><span class="sxs-lookup"><span data-stu-id="e1bf9-168">*AuthentProviderPath* = "c:\\another\\anetCM.dll"</span></span>

 

