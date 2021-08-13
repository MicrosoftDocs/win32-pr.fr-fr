---
title: Classe Win32_TSGatewayServer
description: Utilisé pour les opérations spécifiques au serveur de passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer de la classe Services Bureau à distance
- Win32_TSGatewayServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cd6c24447e7ba3bc22788484b2ac9e437ee947243c17a676728d2a336bd326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603885"
---
# <a name="win32_tsgatewayserver-class"></a>\_Classe TSGatewayServer Win32

Utilisé pour les opérations spécifiques au serveur de passerelle Bureau à distance (passerelle Bureau à distance).

## <a name="syntax"></a>Syntaxe

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSGatewayServer** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ TSGatewayServer** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSelfSignedCertificate**](createselfsignedcertificate-win32-tsgatewayserver.md) | Crée un certificat auto-signé avec un nom d’objet donné et retourne le hachage de certificat en tant que paramètre « out ».<br/> |
| [**Exporter**](export-win32-tsgatewayserver.md)                                           | Retourne la configuration du serveur de passerelle Bureau à distance sous la forme d’une chaîne XML.<br/>                                                       |
| [**Port**](import-win32-tsgatewayserver.md)                                           | Importe une configuration donnée sur le serveur de passerelle Bureau à distance.<br/>                                                             |



 

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

