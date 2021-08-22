---
title: Génération de l’UUID
description: La première étape de la définition de l’interface consiste à utiliser l’utilitaire uuidgen pour générer un identificateur unique universel (UUID).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- Appel de procédure distante RPC, tâches, génération de l’UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c1fbb257a4ce41a4fc0159f703a01705b4dd5926356d7850ec4ce1e0d2e002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929526"
---
# <a name="generating-the-uuid"></a>Génération de l’UUID

La première étape de la définition de l’interface consiste à utiliser l’utilitaire **uuidgen** pour générer un identificateur unique universel (UUID). Un UUID permet aux applications clientes et serveur de les identifier mutuellement. L’utilitaire **uuidgen** (Uuidgen.exe) est installé automatiquement lorsque vous installez le kit de développement logiciel (SDK) de la plateforme.

La commande suivante génère un UUID et crée un fichier de modèle appelé Hello. idl.

**uuidgen/i/ohello.idl**

Votre modèle Hello. idl aura l’aspect suivant (avec un UUID différent, bien sûr).

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




