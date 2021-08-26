---
description: La table AppId ou la table Registry spécifie que le programme d’installation doit configurer et inscrire les serveurs DCOM pour effectuer l’une des opérations suivantes au cours d’une installation.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Table AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a121e6252c6054d5ac2765a9649e345035dde
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882217"
---
# <a name="appid-table"></a>Table AppId

La table AppId ou la [table Registry](registry-table.md) spécifie que le programme d’installation doit configurer et inscrire les serveurs DCOM pour effectuer l’une des opérations suivantes au cours d’une installation.

-   Exécutez le serveur DCOM sous une identité différente de celle de l’utilisateur qui a activé le serveur. Par exemple, pour configurer un serveur DCOM pour qu’il s’exécute toujours en tant qu’utilisateur interactif ou en tant qu’utilisateur prédéfini.
-   Exécutez le serveur DCOM en tant que service.
-   Configurez l’accès de sécurité par défaut pour le serveur DCOM.
-   Inscrire le serveur DCOM de manière à ce qu’il soit activé sur un autre ordinateur.

Cette table est traitée lors de l’installation du composant associé au serveur DCOM dans la \_ colonne composant de la [table de classe](class-table.md). Un AppId n’est pas publié.

La table AppId contient les colonnes suivantes.



| Colonne               | Type                       | Clé : | Nullable |
|----------------------|----------------------------|-----|----------|
| AppId                | [GUID](guid.md)           | O   | N        |
| RemoteServerName     | [Correct](formatted.md) | N   | O        |
| LocalService         | [Text](text.md)           | N   | O        |
| ServiceParameters    | [Text](text.md)           | N   | O        |
| DllSurrogate         | [Text](text.md)           | N   | O        |
| ActivateAtStorage    | [Integer](integer.md)     | N   | O        |
| RunAsInteractiveUser | [Integer](integer.md)     | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId
</dt> <dd>

La colonne AppId de la [table de classe](class-table.md) est une clé étrangère dans cette colonne de la table AppID. Cette colonne contient la valeur AppId qui sera écrite sous le CLSID et crée la clé de GUID AppId sous HKCR \\ AppID.

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName
</dt> <dd>

Cette colonne contient la valeur « RemoteServerName » = &lt; xxxx &gt; qui sera écrite sous HKCR \\ AppID \\ {AppID} \\ .

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>Local
</dt> <dd>

Cette colonne contient la valeur LocalService qui sera écrite sous HKCR \\ AppID \\ { &lt; AppID &gt; } "LocalService" = &lt; xxx &gt; .

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters
</dt> <dd>

Cette colonne contient la valeur de ServiceParameters qui sera écrite sous HKCR \\ AppID \\ {AppID>} "ServiceParameters".

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate
</dt> <dd>

Cette colonne contient la valeur de DllSurrogate qui sera écrite sous HKCR \\ AppID \\ { &lt; AppID &gt; } "DllSurrogate" = &lt; xxx &gt; . Si cette colonne est présente, il s’agit généralement d’une chaîne vide.

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage
</dt> <dd>

une valeur entière différente de zéro dans ce champ amène Windows Installer à écrire HKCR \\ AppID \\ { &lt; appid &gt; } "ActivateAtStorage" = "Y" dans le registre. Si le champ est laissé vide ou a une valeur égale à zéro, aucune valeur ne sera écrite.

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser
</dt> <dd>

une valeur entière différente de zéro dans ce champ amène Windows Installer à écrire HKCR \\ AppID \\ {appid>} "RunAs" = "Interactive User" dans le registre. Si le champ est laissé vide ou a une valeur égale à zéro, aucune valeur ne sera écrite.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette table est utilisée par l' [action RegisterClassInfo](registerclassinfo-action.md) et l' [action UnregisterClassInfo](unregisterclassinfo-action.md).

Notez que la table AppId n’a pas de colonne pour l’enregistrement d’un nom par défaut. Par conséquent, dans les cas où vous devez écrire un nom convivial en tant que valeur de nom par défaut, vous devez vous inscrire à l’aide de la [table du Registre](registry-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



