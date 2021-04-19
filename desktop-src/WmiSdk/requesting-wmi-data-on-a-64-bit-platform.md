---
description: Par défaut, une application ou un script reçoit des données du fournisseur correspondant lorsque deux versions de fournisseurs existent.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Demande de données WMI sur une plateforme 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd392d482f083a3c1b1dff3b90d70f1857aeebb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534432"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="7db77-103">Demande de données WMI sur une plateforme 64 bits</span><span class="sxs-lookup"><span data-stu-id="7db77-103">Requesting WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="7db77-104">Par défaut, une application ou un script reçoit des données du fournisseur correspondant lorsque deux versions de fournisseurs existent.</span><span class="sxs-lookup"><span data-stu-id="7db77-104">By default, an application or script receives data from the corresponding provider when two versions of providers exist.</span></span> <span data-ttu-id="7db77-105">Le fournisseur 32 bits retourne des données à une application 32 bits, y compris tous les scripts, et le fournisseur 64 bits retourne des données aux applications compilées de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7db77-105">The 32-bit provider returns data to a 32-bit application, including all scripts, and the 64-bit provider returns data to the 64-bit compiled applications.</span></span> <span data-ttu-id="7db77-106">Toutefois, une application ou un script peut demander des données à partir du fournisseur non défini par défaut, s’il existe, en avertissant WMI par le biais d’indicateurs sur les appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="7db77-106">However, an application or script can request data from the nondefault provider, if it exists, by notifying WMI through flags on method calls.</span></span>

## <a name="context-flags"></a><span data-ttu-id="7db77-107">Indicateurs de contexte</span><span class="sxs-lookup"><span data-stu-id="7db77-107">Context Flags</span></span>

<span data-ttu-id="7db77-108">Les indicateurs de chaîne **\_ \_ ProviderArchitecture** et **\_ \_ RequiredArchitecture** ont un ensemble de valeurs gérées par WMI, mais non définies dans les fichiers d’en-tête ou de bibliothèque de types du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="7db77-108">The **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** string flags have a set of values handled by WMI but not defined in SDK header or type library files.</span></span> <span data-ttu-id="7db77-109">Les valeurs sont placées dans un paramètre de contexte pour signaler à WMI qu’il doit demander des données à partir du fournisseur non défini par défaut.</span><span class="sxs-lookup"><span data-stu-id="7db77-109">The values are placed in a context parameter to signal WMI that it should request data from the nondefault provider.</span></span>

<span data-ttu-id="7db77-110">La liste suivante répertorie les indicateurs et leurs valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="7db77-110">The following lists the flags and their possible values.</span></span>

<dl> <dt>

<span data-ttu-id="7db77-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span><span class="sxs-lookup"><span data-stu-id="7db77-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="7db77-112">Valeur entière, 32 ou 64, qui spécifie la version 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7db77-112">Integer value, either 32 or 64, that specifies the 32-bit or 64-bit version.</span></span>

</dd> <dt>

<span data-ttu-id="7db77-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span><span class="sxs-lookup"><span data-stu-id="7db77-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="7db77-114">Valeur booléenne utilisée en plus de **\_ \_ ProviderArchitecture** pour forcer le chargement de la version de fournisseur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7db77-114">Boolean value used in addition to **\_\_ProviderArchitecture** to force load the specified provider version.</span></span> <span data-ttu-id="7db77-115">Si la version n’est pas disponible, WMI retourne l’erreur 0x80041013, **wbemErrProviderLoadFailure** pour Visual Basic et **l' \_ \_ échec du \_ chargement \_ du fournisseur WBEM E** pour C++.</span><span class="sxs-lookup"><span data-stu-id="7db77-115">If the version is unavailable, then WMI returns the error 0x80041013, **wbemErrProviderLoadFailure** for Visual Basic and **WBEM\_E\_PROVIDER\_LOAD\_FAILURE** for C++.</span></span> <span data-ttu-id="7db77-116">La valeur par défaut de cet indicateur lorsqu’il n’est pas spécifié est **false**.</span><span class="sxs-lookup"><span data-stu-id="7db77-116">The default value for this flag when it is not specified is **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="7db77-117">Sur un système 64 bits qui possède des versions côte à côte d’un fournisseur, une application ou un script 32 bits reçoit automatiquement des données du fournisseur 32 bits, sauf si ces indicateurs sont fournis et indiquent que les données du fournisseur 64 bits doivent être retournées.</span><span class="sxs-lookup"><span data-stu-id="7db77-117">On a 64-bit system that has side-by-side versions of a provider, a 32-bit application or script automatically receives data from the 32-bit provider, unless these flags are supplied and indicate that the 64-bit provider data should be returned.</span></span>

## <a name="using-the-context-flags"></a><span data-ttu-id="7db77-118">Utilisation des indicateurs de contexte</span><span class="sxs-lookup"><span data-stu-id="7db77-118">Using the Context Flags</span></span>

<span data-ttu-id="7db77-119">Les applications C++ peuvent utiliser l’interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) avec [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) pour communiquer l’utilisation d’un fournisseur qui n’est pas un fournisseur par défaut à WMI.</span><span class="sxs-lookup"><span data-stu-id="7db77-119">C++ applications can use the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface with [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) to communicate the use of a nondefault provider to WMI.</span></span>

<span data-ttu-id="7db77-120">Dans les scripts et les Visual Basic, vous devez créer un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) contenant les indicateurs pour le paramètre *ObjWbemNamedValueSet* de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="7db77-120">In scripting and Visual Basic, you must create a [**SWbemNamedValueSet**](swbemnamedvalueset.md) object containing the flags for the *objWbemNamedValueSet* parameter of [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="7db77-121">Pour plus d’informations sur la configuration des objets de paramètres pour cet appel, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7db77-121">For more information about setting up the parameters objects for this call, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="7db77-122">Vous pouvez exécuter des scripts et des applications en toute sécurité à l’aide des indicateurs de contexte dans les systèmes d’exploitation plus anciens, car WMI les ignore dans les systèmes dans lesquels ils ne sont pas implémentés.</span><span class="sxs-lookup"><span data-stu-id="7db77-122">You can safely run scripts and applications using the context flags in older operating systems, because WMI ignores them in systems in which they are not implemented.</span></span> <span data-ttu-id="7db77-123">Alors que les versions 32 bits et 64 bits du fournisseur de Registre système existent, Notez qu’il n’existe qu’une seule version de l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="7db77-123">While 32-bit and 64-bit versions of the System Registry provider exist, note that only one version of the WMI repository exists.</span></span>

## <a name="accessing-the-default-registry-hive"></a><span data-ttu-id="7db77-124">Accès à la ruche du Registre par défaut</span><span class="sxs-lookup"><span data-stu-id="7db77-124">Accessing the Default Registry Hive</span></span>

<span data-ttu-id="7db77-125">La série d’exemples suivante utilise le [fournisseur Registry](/previous-versions/windows/desktop/regprov/system-registry-provider), qui a des versions 32 bits et 64 bits côte à côte préinstallées sur les systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7db77-125">The following series of examples use the [Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which has side-by-side 32-bit and 64-bit versions preinstalled on 64-bit operating systems.</span></span> <span data-ttu-id="7db77-126">Dans ces exemples, les clients 32 bits obtiennent les données retournées par le fournisseur à partir du nœud 32-bit **\_ \_ \\ \\ Wow6432Node \\ Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="7db77-126">In these examples, 32-bit clients get data returned by the provider from the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft**.</span></span> <span data-ttu-id="7db77-127">les clients 64 bits obtiennent les données retournées par le fournisseur à partir du nœud 64-bit de la **\_ \_ \\ \\ \\ journalisation Microsoft du logiciel de l’ordinateur local**.</span><span class="sxs-lookup"><span data-stu-id="7db77-127">64-bit clients get data returned by the provider from the 64-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Logging**.</span></span>

<span data-ttu-id="7db77-128">Les scripts montrent comment appeler les méthodes de la classe Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) via [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) pour obtenir des données à partir de la ruche de Registre 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7db77-128">The scripts show how to call the methods of the Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class through [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to obtain data from the 32-bit registry hive.</span></span>

<span data-ttu-id="7db77-129">Le script suivant récupère les données du fournisseur qui correspondent à la largeur en bits de l’appelant, dans ce cas 64 bits, car il s’agit d’un script s’exécutant sous l’hôte WSH (Windows Script Host) 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7db77-129">The following script gets back data from the provider that matches the bit width of the caller, in this case 64 bits, because it is a script running under the 64-bit Windows Script Host (WSH).</span></span> <span data-ttu-id="7db77-130">Le script obtient la valeur du nœud de Registre 64 de la clé **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM \\ Logging** plutôt que le nœud 32-bit **HKEY \_ local \_ machine \\ Software \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="7db77-130">The script gets the value from the 64-bit registry node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM\\Logging** rather than the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\WBEM\\CIMOM**.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objReg = Getobject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\default:stdregprov")
'Set up inParameters object
Set Inparams = objReg.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objReg.ExecMethod_("GetStringValue", Inparams)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



<span data-ttu-id="7db77-131">Si la valeur de **journalisation** dans la ruche par défaut est définie sur 1, la sortie du script doit ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7db77-131">If the **Logging** value in the default hive is set to 1, then the output from the script should look something like the following:</span></span>

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="7db77-132">Exemple : demander spécifiquement la ruche de Registre 32 bits sur un ordinateur 64 bits</span><span class="sxs-lookup"><span data-stu-id="7db77-132">Example: Specifically Requesting the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="7db77-133">L’exemple modifié suivant du script par défaut utilise l’indicateur de chaîne **\_ \_ ProviderArchitecture** pour demander l’accès aux données de Registre 32 bits sur un ordinateur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7db77-133">The following modified example of the default script uses the **\_\_ProviderArchitecture** string flag to request access to the 32-bit registry data on a 64-bit computer.</span></span> <span data-ttu-id="7db77-134">L’appelant est connecté à la ruche 32 bits, qu’il s’agisse d’une application 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7db77-134">The caller is connected to the 32-bit hive irrespective of whether it is a 32- or 64-bit application.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="7db77-135">Exemple : forcer WMI à accéder à la ruche de Registre 32 bits sur un ordinateur 64 bits</span><span class="sxs-lookup"><span data-stu-id="7db77-135">Example: Forcing WMI to Access the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="7db77-136">La modification suivante du script ci-dessus en ajoutant les indicateurs **\_ \_ ProviderArchitecture** et **\_ \_ RequiredArchitecture** au paramètre context force WMI à charger le fournisseur 32 bits et à récupérer les données 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7db77-136">The following modification of the script above by adding the **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** flags to the context parameter forces WMI to load the 32-bit provider and get 32-bit data.</span></span> <span data-ttu-id="7db77-137">Si le fournisseur n’existe pas, une erreur de chargement du fournisseur se produit.</span><span class="sxs-lookup"><span data-stu-id="7db77-137">If the provider does not exist, then a provider load error occurs.</span></span> <span data-ttu-id="7db77-138">L’objet de contexte doit être fourni dans la connexion à WMI en appelant [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="7db77-138">The context object must be supplied in the connection to WMI by calling [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
objCtx.Add "__RequiredArchitecture", TRUE
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

' Use ExecMethod to call the GetStringValue method
Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="related-topics"></a><span data-ttu-id="7db77-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7db77-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7db77-140">Obtention et fourniture de données sur un ordinateur 64 bits</span><span class="sxs-lookup"><span data-stu-id="7db77-140">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
