---
description: Cette classe est la classe parente pour les événements d’image. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Classe Image
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973307"
---
# <a name="image-class"></a>Classe Image

Cette classe est la classe parente pour les événements d’image.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **image** ne définit aucun membre.

## <a name="remarks"></a>Notes

Pour activer les événements d’image dans une session de journalisation du noyau NT, spécifiez l’indicateur de chargement d’image de l’indicateur de trace d’événements dans le membre **EnableFlags** de la structure des [**Propriétés de \_ trace \_ d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . **\_ \_ \_ \_**

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de chargement d’image en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**ImageLoadGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier les événements de chargement d’image lors de l’utilisation d’événements.



| Type d'événement                                                          | Description                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Événement \_ Type de TRACE \_ \_ Load**(la valeur de type d’événement est 10)<br/>     | Événement de chargement d’image. Généré lors du chargement d’une DLL ou d’un fichier exécutable. Le fournisseur génère un seul événement pour la première fois qu’une DLL donnée est chargée. La classe MOF de [**\_ chargement d’image**](image-load.md) définit les données d’événement pour cet événement.      |
| **Événement \_ \_ \_ Fin du type de suivi**(la valeur du type d’événement est 2)<br/>       | Événement de déchargement d’image. Généré lorsqu’une DLL ou un fichier exécutable est déchargé. Le fournisseur génère un seul événement pour la dernière fois qu’une DLL donnée est déchargée. La classe MOF de [**\_ chargement d’image**](image-load.md) définit les données d’événement pour cet événement. |
| **Événement \_ Type de suivi \_ \_ DC \_ Start**(la valeur du type d’événement est 3)<br/> | Événement de démarrage de la collecte de données. Énumère toutes les images chargées au début de la trace. La classe MOF de [**\_ chargement d’image**](image-load.md) définit les données d’événement pour cet événement.                                                                  |
| **Événement \_ \_Type de \_ trace \_ end DC**(la valeur du type d’événement est 4)<br/>   | Événement de fin de la collecte de données. Énumère toutes les images chargées à la fin de la trace. La classe MOF de [**\_ chargement d’image**](image-load.md) définit les données d’événement pour cet événement.                                                                          |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Chargement d’image \_**](image-load.md)
</dt> <dt>

[**Image \_ v0**](image-v0.md)
</dt> <dt>

[**Image \_ v1**](image-v1.md)
</dt> </dl>

 

 
