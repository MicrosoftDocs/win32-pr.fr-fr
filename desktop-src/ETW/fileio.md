---
description: Cette classe est la classe parente pour les événements d’e/s de fichier. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: FileIo (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f7c032cb7af325efa1d2ea76702068fc7b3be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972798"
---
# <a name="fileio-class"></a>FileIo (classe)

Cette classe est la classe parente pour les événements d’e/s de fichier.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **FileIo** ne définit aucun membre.

## <a name="remarks"></a>Notes

Pour activer les événements d’e/s de fichier dans une session de journalisation du noyau NT, spécifiez l’indicateur d' **\_ \_ \_ \_ \_ e/s de fichier disque** de l’indicateur de trace d’événements dans le membre **EnableFlags** d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . Vous pouvez également spécifier un ou plusieurs des indicateurs suivants :

-   **\_ \_ \_ e/s de fichier d’indicateur de trace d’événements \_**
-   **événement d’indicateur de trace d’événements \_ \_ \_ \_ \_ init**

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements d’e/s de fichier en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**FileIoGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement réel lors de la consommation d’événements.



| Type d'événement             | Description                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La valeur du type d’événement est 0  | Événement de nom de fichier. La classe MOF [**\_ nom FileIo**](fileio-name.md) définit les données d’événement pour cet événement.                                                                               |
| La valeur du type d’événement est 32 | Événement de création de fichier. La classe MOF [**\_ nom FileIo**](fileio-name.md) définit les données d’événement pour cet événement.                                                                             |
| La valeur du type d’événement est 35 | Événement de suppression de fichier. La classe MOF [**\_ nom FileIo**](fileio-name.md) définit les données d’événement pour cet événement.                                                                             |
| La valeur du type d’événement est 36 | Événement d’arrêt de fichier. Énumère tous les fichiers ouverts sur l’ordinateur à la fin de la session de suivi. La classe MOF [**\_ nom FileIo**](fileio-name.md) définit les données d’événement pour cet événement. |
| La valeur du type d’événement est 64 | Événement de création de fichier. La classe [**FileIo \_ Create**](fileio-create.md) MOF définit les données d’événement pour cet événement.                                                                         |
| La valeur du type d’événement est 72 | Événement d’énumération de répertoire. La [**classe \_ DirEnum FileIo de FileIo**](fileio-direnum.md) définit les données d’événement pour cet événement.                                                             |
| La valeur du type d’événement est 77 | Événement de notification d’annuaire. La [**classe \_ DirEnum FileIo de FileIo**](fileio-direnum.md) définit les données d’événement pour cet événement.                                                            |
| La valeur du type d’événement est 69 | Définir un événement d’informations. La classe MOF [**\_ info de FileIo**](fileio-info.md) définit les données d’événement pour cet événement.                                                                         |
| La valeur du type d’événement est 70 | Supprimer un événement de fichier. La classe MOF [**\_ info de FileIo**](fileio-info.md) définit les données d’événement pour cet événement.                                                                             |
| La valeur du type d’événement est 71 | Renommer l’événement de fichier. La classe MOF [**\_ info de FileIo**](fileio-info.md) définit les données d’événement pour cet événement.                                                                             |
| La valeur du type d’événement est 74 | Événement d’informations de fichier de requête. La classe MOF [**\_ info de FileIo**](fileio-info.md) définit les données d’événement pour cet événement.                                                                  |
| La valeur du type d’événement est 75 | Événement de contrôle du système de fichiers. La classe MOF [**\_ info de FileIo**](fileio-info.md) définit les données d’événement pour cet événement.                                                                     |
| La valeur du type d’événement est 76 | Événement de fin d’opération. La classe MOF [**\_ ouverte FileIo**](fileio-opend.md) définit les données d’événement pour cet événement.                                                                      |
| La valeur du type d’événement est 67 | Événement de lecture de fichier. La classe MOF [**\_ ReadWrite de FileIo**](fileio-readwrite.md) définit les données d’événement pour cet événement.                                                                     |
| La valeur du type d’événement est 68 | Événement d’écriture de fichier. La classe MOF [**\_ ReadWrite de FileIo**](fileio-readwrite.md) définit les données d’événement pour cet événement.                                                                    |
| La valeur du type d’événement est 65 | Événement de nettoyage. L’événement est généré lorsque le dernier handle du fichier est libéré. La [**classe \_ SimpleOp FileIo de FileIo**](fileio-simpleop.md) définit les données d’événement pour cet événement.   |
| La valeur du type d’événement est 66 | Événement de fermeture. L’événement est généré lorsque l’objet fichier est libéré. La [**classe \_ SimpleOp FileIo de FileIo**](fileio-simpleop.md) définit les données d’événement pour cet événement.                     |
| La valeur du type d’événement est 73 | Événement de vidage. Cet événement est généré lorsque les mémoires tampons de fichier sont entièrement vidées sur le disque. La [**classe \_ SimpleOp FileIo de FileIo**](fileio-simpleop.md) définit les données d’événement pour cet événement.  |



 

Les événements d’e/s de fichier sont journalisés au début de l’opération.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**FileIo \_ v0**](fileio-v0.md)
</dt> <dt>

[**FileIo \_ v1**](fileio-v1.md)
</dt> </dl>

 

 
