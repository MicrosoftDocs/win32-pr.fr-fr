---
title: Classe MSAD_ReplCursor
description: Fournit des informations d’état de réplication entrante sur tous les réplicas d’un contexte d’appellation (NC) donné.
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor de la classe Active Directory
- MSAD_ReplCursor de la classe Active Directory, Description
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c001adf774321ba61e232298d070fb4a29d4b3f0740dd8ef900ff4ea0b4cb83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186064"
---
# <a name="msad_replcursor-class"></a>MSAD \_ ReplCursor, classe

Fournit des informations d’état de réplication entrante sur tous les réplicas d’un contexte d’appellation (NC) donné.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a>Membres

La classe **MSAD \_ ReplCursor** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSAD \_ ReplCursor** possède les propriétés suivantes.

<dl> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient le chemin d’accès X. 500 pour le contexte d’appellation (NC) qui contient ce curseur.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le chemin d’accès X. 500 pour l’agent de système d’annuaire (DSA) qui représente le contrôleur de domaine source.

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient l’identificateur d’appel du serveur d’origine auquel correspond le **USNAttributeFilter** .

</dd> <dt>

**TimeOfLastSuccessfulSync**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’horodateur de la dernière synchronisation de réplication réussie avec le DSA source. Indique l’heure de la dernière modification apportée par ce contrôleur de périphérique sur le DSA source pour ce contexte de nommage.

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le numéro de séquence de mise à jour maximal sur lequel le serveur de destination peut indiquer qu’il a enregistré toutes les modifications apportées par le serveur donné aux numéros de séquence de mise à jour inférieurs ou égaux à ce numéro de séquence de mise à jour. Cette propriété est utilisée pour filtrer les modifications que le serveur de destination a déjà appliquées sur les serveurs sources de réplication.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\MicrosoftActiveDirectory racine<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_curseur de réplication DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

