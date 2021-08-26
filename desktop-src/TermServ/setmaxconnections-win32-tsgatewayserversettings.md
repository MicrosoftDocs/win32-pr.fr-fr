---
title: Méthode SetMaxConnections de la classe Win32_TSGatewayServerSettings
description: Définit les propriétés MaxConnections et UnlimitedConnections, qui contrôlent le nombre maximal de connexions autorisées sur le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetMaxConnections
- Services Bureau à distance de la méthode SetMaxConnections, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode SetMaxConnections
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e241b137f2a3a061be06538b934c163ea6445ff177fecf9aaf4dc7db5367990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009043"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a>Méthode SetMaxConnections de la \_ classe Win32 TSGatewayServerSettings

Définit les propriétés **MaxConnections** et **UnlimitedConnections** , qui contrôlent le nombre maximal de connexions autorisées sur le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Connexions* \[ dans\]
</dt> <dd>

Nombre de connexions que ce serveur doit accepter. Pour un nombre illimité de connexions, affectez la valeur **true** au paramètre *IsUnlimited* .

</dd> <dt>

*IsUnlimited* \[ dans\]
</dt> <dd>

Si la **valeur est true**, les connexions au service ne sont pas limitées à un nombre spécifique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne zéro. Si la méthode échoue, elle retourne une valeur différente de zéro. Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

