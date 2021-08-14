---
description: Cette classe est la classe parente pour les événements d’e/s de disque. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: E, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0e91f5e8b84d77b0938f35da69a84c26fa0f34a4da63bce40330484a29e19b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395300"
---
# <a name="diskio-class"></a>E, classe

Cette classe est la classe parente pour les événements d’e/s de disque.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **e** ne définit aucun membre.

## <a name="remarks"></a>Remarques

Pour activer les événements d’e/s de disque dans une session de journalisation du noyau NT, spécifiez l’indicateur d' **\_ e/ \_ \_ \_ s disque** de l’indicateur de trace d’événements dans le membre **EnableFlags** d’une structure de [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . Vous pouvez également spécifier un ou plusieurs des indicateurs suivants :

-   **indicateur de trace d’événements, \_ \_ \_ initialisation des \_ e/s disque \_**
-   **\_pilote d' \_ indicateur de trace d’événements \_**

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements d’e/s disque en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**DiskIoGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement d’e/s disque réel lors de la consommation d’événements.



| Type d'événement                                                                      | Description                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Événement \_ \_Lecture des \_ e \_ /s du type de suivi**(la valeur du type d’événement est 10)<br/>             | Événement Read. La classe [**e \_ TypeGroup1**](diskio-typegroup1.md) MOF définit les données d’événement pour cet événement.                                              |
| **Événement \_ Type de TRACE \_ \_ \_ écriture d’e/s**(la valeur du type d’événement est 11)<br/>            | Événement d’écriture. La classe [**e \_ TypeGroup1**](diskio-typegroup1.md) MOF définit les données d’événement pour cet événement.                                             |
| **Événement \_ Type de TRACE \_ \_ e \_ Read \_ init**(type d’événement : valeur 12)<br/>       | Initialise l’événement de lecture. La classe [**e \_ TypeGroup2**](diskio-typegroup2.md) MOF définit les données d’événement pour cet événement.                                   |
| **Événement \_ Type de suivi \_ \_ e/s \_ écriture/écriture \_**(la valeur du type d’événement est 13)<br/>      | Initialise l’événement d’écriture. La classe [**e \_ TypeGroup2**](diskio-typegroup2.md) MOF définit les données d’événement pour cet événement.                                  |
| **Événement \_ Type de TRACE \_ \_ \_ vidage des e/s**(la valeur du type d’événement est 14)<br/>            | Initialise l’événement d’écriture. La classe [**e \_ TypeGroup3**](diskio-typegroup3.md) MOF définit les données d’événement pour cet événement.                                  |
| **Événement \_ Type de suivi \_ \_ IO \_ flush \_ init**(la valeur de type d’événement est 15)<br/>      | Initialise l’événement Flush. La classe [**e \_ TypeGroup2**](diskio-typegroup2.md) MOF définit les données d’événement pour cet événement.                                  |
| **Événement \_ Type de suivi \_ \_ e/s \_ redirigée \_ init**(la valeur du type d’événement est 16)<br/> | Initialise l’événement Redirigé. les événements d’e/s redirigés permettent de mapper le disque IOs à un Format wim (Windows Imaging Format) au nom de fichier dans le fichier wim.                  |
| La valeur du type d’événement est 52<br/>                                               | Événement de demande complète du pilote. La classe MOF [**DriverCompleteRequest**](drivercompleterequest.md) définit les données d’événement pour cet événement.                    |
| La valeur du type d’événement est 53<br/>                                               | Événement de retour de demande complet du pilote. La classe MOF [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) définit les données d’événement pour cet événement. |
| La valeur du type d’événement est 37<br/>                                               | Événement de routine de fin d’exécution du pilote. La classe MOF [**DriverCompletionRoutine**](drivercompletionroutine.md) définit les données d’événement pour cet événement.              |
| La valeur du type d’événement est 34<br/>                                               | Événement d’appel de fonction principale du pilote. La classe MOF [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) définit les données d’événement pour cet événement.             |
| La valeur du type d’événement est 35<br/>                                               | Événement de retour d’appel de fonction principale du pilote. La classe MOF [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) définit les données d’événement pour cet événement.  |



 

Le fournisseur d’e/s disque ne peut pas identifier le fichier qui est lu ou écrit pendant un événement d’e/s disque. Pour récupérer le nom du fichier associé à l’événement d’e/s disque, activez le fournisseur d’événements file I/0.

Les événements d’e/s de disque sont enregistrés au moment de l’exécution des e/s. Pour déterminer à quel moment l’opération d’e/s a commencé, utilisez les événements d’initialisation, par exemple, le type de suivi d’événement \_ \_ \_ IO \_ Read \_ init.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**E \_ TypeGroup1**](diskio-typegroup1.md)
</dt> <dt>

[**E \_ TypeGroup2**](diskio-typegroup2.md)
</dt> <dt>

[**E \_ TypeGroup3**](diskio-typegroup3.md)
</dt> <dt>

[**DriverCompleteRequest**](drivercompleterequest.md)
</dt> <dt>

[**DriverCompleteRequestReturn**](drivercompleterequestreturn.md)
</dt> <dt>

[**DriverCompletionRoutine**](drivercompletionroutine.md)
</dt> <dt>

[**DriverMajorFunctionCall**](drivermajorfunctioncall.md)
</dt> <dt>

[**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
