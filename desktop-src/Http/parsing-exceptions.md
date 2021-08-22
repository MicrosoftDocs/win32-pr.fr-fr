---
title: Analyse des exceptions
description: L’API serveur HTTP fournit des clés de Registre pour prendre en charge l’analyse des exceptions à la spécification HTTP/1.1 pour la compatibilité descendante.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analyse des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b546c5473641bbd5d719908903c2d9e19db25ade2ff6677a5ce5ec7ea472d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950728"
---
# <a name="parsing-exceptions"></a>Analyse des exceptions

L’API serveur HTTP fournit des clés de Registre pour prendre en charge l’analyse des exceptions à la spécification HTTP/1.1 pour la compatibilité descendante. Ces exceptions ne sont pas activées par défaut et doivent être activées au cas par cas, lorsque le serveur rencontre des problèmes de compatibilité avec les clients HTTP. Ces valeurs sont créées sous l’emplacement de Registre suivant :

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

Le tableau suivant répertorie les clés de Registre fournies pour prendre en charge les exceptions répertoriées. Pour activer une exception, affectez la valeur 1 à la valeur de clé correspondante, puis redémarrez le service HTTP.



| Nom de clé                              | Description                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowWeakHeaderNameSyntax (DWORD)     | Permet à l’analyseur HTTP d’accepter les noms d’en-tête avec des caractères de séparation tels que «  ? ».                                                                                                                                                                                                                                                                                            |
| AllowWeakHeaderValueSyntax (DWORD)    | Permet à l’analyseur HTTP d’accepter des valeurs d’en-tête avec des caractères de contrôle bruts (sans séquence d’échappement).                                                                                                                                                                                                                                                                                   |
| AllowCaseInsensitiveVerbs (DWORD)     | Permet à l’analyseur HTTP d’accepter des méthodes/verbes HTTP en minuscules, tels que « récupérer ».                                                                                                                                                                                                                                                                                                    |
| AllowUnEscapedRestrictedChars (DWORD) | Permet à l’analyseur HTTP d’accepter des caractères de contrôle dans ABSPATH et des chaînes de requête de l’URL. Dans le cas d’une URL absolue, les caractères de contrôle ne sont pas autorisés dans le nom d’hôte. Toutes les versions des URL, à savoir UTF8, DBCS et ANSI, autorisent les caractères de contrôle. Tous les caractères de contrôle ASCII, à l’exception de NUL (0x00), LF (0x0A), CR (0x0D) et de la tabulation horizontale (0x09), sont autorisés. |



 

 

 




