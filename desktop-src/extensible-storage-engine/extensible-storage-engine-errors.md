---
description: 'En savoir plus sur : Erreurs du moteur de stockage extensible'
title: Erreurs du moteur de stockage extensible
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868966"
---
# <a name="extensible-storage-engine-errors"></a>Erreurs du moteur de stockage extensible


_**S’applique à :** Windows | Serveur Windows_

## <a name="extensible-storage-engine-errors"></a>Erreurs du moteur de stockage extensible

Toutes les erreurs possibles retournées par l’API ESE (Extensible Storage Engine) sont définies par le type de données [JET_ERR](./jet-err.md) . Pour obtenir la liste des indicateurs d’erreur définis pour cette API, consultez [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md).

Dans la documentation de l’API ESE, seules les erreurs les plus importantes sont documentées. Ces erreurs représentent généralement des erreurs d’utilisation de l’API ou des conditions d’erreur très importantes. N’oubliez pas que ces API ESE peuvent également retourner d’autres erreurs qui ne sont pas documentées pour chaque API. Dans ce cas, l’appelant doit simplement gérer l’erreur, comme pour toute autre erreur retournée par l’API. La valeur d’erreur spécifique peut ensuite être utilisée à des fins de diagnostic telles que le suivi.

En général, une valeur supérieure à zéro doit être interprétée comme un avertissement, une valeur de zéro doit être interprétée comme une réussite et une valeur inférieure à zéro doit être interprétée comme une erreur. Aucun autre modèle dans ces valeurs (par exemple, les plages de valeurs) ne doit être basé sur une application.

Lorsque ESE rencontre certaines des erreurs les plus graves, il crée une entrée dans le journal des événements qui contient des détails sur les erreurs. Le niveau de journalisation peut être contrôlé par les [paramètres du journal des événements](./event-log-parameters.md).

Certaines applications requièrent la possibilité de retourner des [JET_ERR](./jet-err.md)s en tant que HRESULT. L’exemple C++ suivant montre comment effectuer cette conversion :

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

Pour plus d’informations sur la configuration des paramètres système pour la gestion des erreurs, consultez [paramètres de gestion des erreurs](./error-handling-parameters.md).

### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)

[Codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)
