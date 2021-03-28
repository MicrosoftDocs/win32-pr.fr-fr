---
description: Cette classe est la classe parente des événements du Registre. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 362d7653-1ba0-45b7-80f3-0fccca0badf1
title: Classe Registry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6799756ebfe573fad6a32a191e79c3c2b745f563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113579"
---
# <a name="registry-class"></a>Classe Registry

Cette classe est la classe parente des événements du Registre.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(2)]
class Registry : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **Registry** ne définit aucun membre.

## <a name="remarks"></a>Notes

Pour activer les événements de Registre dans une session de journalisation du noyau NT, spécifiez le  Registre de l’indicateur de trace d' **événements \_ \_ \_** dans le membre EnableFlags d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de registre en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**RegistryGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement de Registre réel lors de la consommation d’événements.



| Type d'événement                                                                       | Description                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Événement \_ Type de suivi \_ \_ REGCREATE**(la valeur du type d’événement est 10)<br/>             | Créer un événement clé. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                            |
| **Événement \_ Type de suivi \_ \_ RegDelete**(la valeur du type d’événement est 12)<br/>             | Événement de suppression de clé. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                            |
| **Événement \_ Type de suivi \_ \_ REGDELETEVALUE**(la valeur du type d’événement est 15)<br/>        | Événement de suppression de valeur. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                          |
| **Événement \_ Type de suivi \_ \_ REGENUMERATEKEY**(la valeur du type d’événement est 17)<br/>       | Événement de clé d’énumération. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                         |
| **Événement \_ Type de suivi \_ \_ REGENUMERATEVALUEKEY**(la valeur du type d’événement est 18)<br/>  | Événement d’énumération de la clé de valeur. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                   |
| **Événement \_ Type de suivi \_ \_ REGFLUSH**(la valeur du type d’événement est 21)<br/>              | Événement de clé de vidage. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                             |
| **Événement \_ Type de suivi \_ \_ REGKCBDMP**(la valeur du type d’événement est 22)<br/>             | Créer un événement clé. Généré lorsqu’une opération de Registre utilise des handles plutôt que des chaînes pour référencer des sous-clés. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement. |
| **Événement \_ Type de suivi \_ \_ REGOPEN**(la valeur du type d’événement est 11)<br/>               | Événement d’ouverture de clé. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                              |
| **Événement \_ Type de suivi \_ \_ REGQUERY**(la valeur du type d’événement est 13)<br/>              | Événement de clé de requête. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                             |
| **Événement \_ Type de suivi \_ \_ REGQUERYMULTIPLEVALUE**(la valeur du type d’événement est 19)<br/> | Interroger plusieurs événements de valeur. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                  |
| **Événement \_ Type de suivi \_ \_ REGQUERYVALUE**(la valeur du type d’événement est 16)<br/>         | Événement de valeur de requête. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                           |
| **Événement \_ Type de suivi \_ \_ REGSETINFORMATION**(la valeur du type d’événement est 20)<br/>     | Définir un événement d’informations. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                       |
| **Événement \_ Type de suivi \_ \_ REGSETVALUE**(la valeur du type d’événement est 14)<br/>           | Événement de valeur définie. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                             |
| Valeur de type d’événement, 23                                                             | événement de suppression de clé. Généré lorsqu’une opération de Registre utilise des handles plutôt que des chaînes pour référencer des sous-clés. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement. |
| Valeur de type d’événement, 24                                                             | Énumère les clés de Registre ouvertes au début de la session. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                           |
| Valeur de type d’événement, 25                                                             | Énumère les clés de Registre ouvertes à la fin de la session. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                  |
| Valeur de type d’événement, 26                                                             | La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                                              |
| Valeur de type d’événement, 27                                                             | Événement d’ouverture de clé. La classe de [**Registre \_ TypeGroup1**](registry-typegroup1.md) MOF définit les données d’événement pour cet événement.                                                                                              |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Registre \_ TypeGroup1**](registry-typegroup1.md)
</dt> <dt>

[**Registre \_ v0**](registry-v0.md)
</dt> <dt>

[**Registre \_ v1**](registry-v1.md)
</dt> </dl>

 

 
