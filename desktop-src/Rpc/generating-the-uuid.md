---
title: Génération de l’UUID
description: La première étape de la définition de l’interface consiste à utiliser l’utilitaire uuidgen pour générer un identificateur unique universel (UUID).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- Appel de procédure distante RPC, tâches, génération de l’UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194235"
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

 

 




