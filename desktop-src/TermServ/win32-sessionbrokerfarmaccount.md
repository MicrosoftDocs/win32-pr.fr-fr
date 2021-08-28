---
title: Classe Win32_SessionBrokerFarmAccount
description: La \_ classe SessionBrokerFarmAccount Win32 n’est plus disponible pour une utilisation à partir de Windows Server 2012. | Classe Win32_SessionBrokerFarmAccount
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarmAccount de la classe Services Bureau à distance
- Win32_SessionBrokerFarmAccount de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b7d55f973dc19c03182a4199b64f91f9de5a0774cc8c8f9d77d67eeb715c24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422489"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a>\_Classe SessionBrokerFarmAccount Win32

\[La **classe \_ SessionBrokerFarmAccount Win32** n’est plus disponible pour une utilisation à partir de Windows Server 2012.\]

Définit un compte de batterie session Broker.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ SessionBrokerFarmAccount** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ SessionBrokerFarmAccount** possède ces méthodes.



| Méthode                                                      | Description                          |
|:------------------------------------------------------------|:-------------------------------------|
| [**DeleteEx**](deleteex-win32-sessionbrokerfarmaccount.md) | Supprime le compte de batterie de serveurs.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **Win32 \_ SessionBrokerFarmAccount** a ces propriétés.

<dl> <dt>

**AccountDomain**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom du domaine auquel appartient le compte de batterie de serveurs.

</dd> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom du compte de batterie de serveurs.

</dd> <dt>

**AccountPassword**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Mot de passe du compte de batterie de serveurs.

</dd> <dt>

**AccountSPN1**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Premier nom de principal du service (SPN) associé au compte de la batterie de serveurs.

</dd> <dt>

**AccountSPN2**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Deuxième SPN associé au compte de batterie de serveurs.

</dd> <dt>

**ComputerDNSName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom DNS de l’ordinateur associé au compte de la batterie de serveurs.

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom de la batterie de serveurs session Broker.

</dd> <dt>

**Manuel**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le mot de passe du compte est mis à jour manuellement.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Fin de la prise en charge des clients<br/>    | Aucun pris en charge<br/>                                                              |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/>                                                      |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

