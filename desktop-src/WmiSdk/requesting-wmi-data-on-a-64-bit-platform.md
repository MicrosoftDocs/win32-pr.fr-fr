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
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a>Demande de données WMI sur une plateforme 64 bits

Par défaut, une application ou un script reçoit des données du fournisseur correspondant lorsque deux versions de fournisseurs existent. Le fournisseur 32 bits retourne des données à une application 32 bits, y compris tous les scripts, et le fournisseur 64 bits retourne des données aux applications compilées de 64 bits. Toutefois, une application ou un script peut demander des données à partir du fournisseur non défini par défaut, s’il existe, en avertissant WMI par le biais d’indicateurs sur les appels de méthode.

## <a name="context-flags"></a>Indicateurs de contexte

Les indicateurs de chaîne **\_ \_ ProviderArchitecture** et **\_ \_ RequiredArchitecture** ont un ensemble de valeurs gérées par WMI, mais non définies dans les fichiers d’en-tête ou de bibliothèque de types du kit de développement logiciel (SDK). Les valeurs sont placées dans un paramètre de contexte pour signaler à WMI qu’il doit demander des données à partir du fournisseur non défini par défaut.

La liste suivante répertorie les indicateurs et leurs valeurs possibles.

<dl> <dt>

<span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**
</dt> <dd>

Valeur entière, 32 ou 64, qui spécifie la version 32 bits ou 64 bits.

</dd> <dt>

<span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**
</dt> <dd>

Valeur booléenne utilisée en plus de **\_ \_ ProviderArchitecture** pour forcer le chargement de la version de fournisseur spécifiée. Si la version n’est pas disponible, WMI retourne l’erreur 0x80041013, **wbemErrProviderLoadFailure** pour Visual Basic et **l' \_ \_ échec du \_ chargement \_ du fournisseur WBEM E** pour C++. La valeur par défaut de cet indicateur lorsqu’il n’est pas spécifié est **false**.

</dd> </dl>

Sur un système 64 bits qui possède des versions côte à côte d’un fournisseur, une application ou un script 32 bits reçoit automatiquement des données du fournisseur 32 bits, sauf si ces indicateurs sont fournis et indiquent que les données du fournisseur 64 bits doivent être retournées.

## <a name="using-the-context-flags"></a>Utilisation des indicateurs de contexte

Les applications C++ peuvent utiliser l’interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) avec [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) pour communiquer l’utilisation d’un fournisseur qui n’est pas un fournisseur par défaut à WMI.

Dans les scripts et les Visual Basic, vous devez créer un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) contenant les indicateurs pour le paramètre *ObjWbemNamedValueSet* de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md). Pour plus d’informations sur la configuration des objets de paramètres pour cet appel, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

Vous pouvez exécuter des scripts et des applications en toute sécurité à l’aide des indicateurs de contexte dans les systèmes d’exploitation plus anciens, car WMI les ignore dans les systèmes dans lesquels ils ne sont pas implémentés. Alors que les versions 32 bits et 64 bits du fournisseur de Registre système existent, Notez qu’il n’existe qu’une seule version de l’espace de stockage WMI.

## <a name="accessing-the-default-registry-hive"></a>Accès à la ruche du Registre par défaut

La série d’exemples suivante utilise le [fournisseur Registry](/previous-versions/windows/desktop/regprov/system-registry-provider), qui a des versions 32 bits et 64 bits côte à côte préinstallées sur les systèmes d’exploitation 64 bits. Dans ces exemples, les clients 32 bits obtiennent les données retournées par le fournisseur à partir du nœud 32-bit **\_ \_ \\ \\ Wow6432Node \\ Microsoft**. les clients 64 bits obtiennent les données retournées par le fournisseur à partir du nœud 64-bit de la **\_ \_ \\ \\ \\ journalisation Microsoft du logiciel de l’ordinateur local**.

Les scripts montrent comment appeler les méthodes de la classe Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) via [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) pour obtenir des données à partir de la ruche de Registre 32 bits.

Le script suivant récupère les données du fournisseur qui correspondent à la largeur en bits de l’appelant, dans ce cas 64 bits, car il s’agit d’un script s’exécutant sous l’hôte WSH (Windows Script Host) 64 bits. Le script obtient la valeur du nœud de Registre 64 de la clé **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM \\ Logging** plutôt que le nœud 32-bit **HKEY \_ local \_ machine \\ Software \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM**.


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



Si la valeur de **journalisation** dans la ruche par défaut est définie sur 1, la sortie du script doit ressembler à ce qui suit :

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Exemple : demander spécifiquement la ruche de Registre 32 bits sur un ordinateur 64 bits

L’exemple modifié suivant du script par défaut utilise l’indicateur de chaîne **\_ \_ ProviderArchitecture** pour demander l’accès aux données de Registre 32 bits sur un ordinateur 64 bits. L’appelant est connecté à la ruche 32 bits, qu’il s’agisse d’une application 32 ou 64 bits.


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



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Exemple : forcer WMI à accéder à la ruche de Registre 32 bits sur un ordinateur 64 bits

La modification suivante du script ci-dessus en ajoutant les indicateurs **\_ \_ ProviderArchitecture** et **\_ \_ RequiredArchitecture** au paramètre context force WMI à charger le fournisseur 32 bits et à récupérer les données 32 bits. Si le fournisseur n’existe pas, une erreur de chargement du fournisseur se produit. L’objet de contexte doit être fourni dans la connexion à WMI en appelant [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Obtention et fourniture de données sur un ordinateur 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
