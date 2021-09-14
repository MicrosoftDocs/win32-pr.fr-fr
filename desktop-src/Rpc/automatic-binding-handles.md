---
title: Handles de liaison automatiques
description: Les handles de liaison automatiques sont utiles lorsque l’application ne nécessite pas de serveur spécifique et lorsqu’il n’est pas nécessaire de conserver les informations d’État entre le client et le serveur.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416617"
---
# <a name="automatic-binding-handles"></a>Handles de liaison automatiques

Les handles de liaison automatiques sont utiles lorsque l’application ne nécessite pas de serveur spécifique et lorsqu’il n’est pas nécessaire de conserver les informations d’État entre le client et le serveur. Lorsque vous utilisez un handle de liaison automatique, vous n’êtes pas obligé d’écrire du code d’application cliente pour gérer la liaison et les handles. il vous suffit de spécifier l’utilisation du handle de liaison automatique dans le fichier de configuration de l’application (ACF). Le stub définit ensuite le handle et gère la liaison.

Par exemple, une opération d’horodatage peut être implémentée à l’aide d’un handle automatique. Il ne fait aucune différence avec l’application cliente que le serveur lui fournit avec l’horodatage, car elle peut accepter l’heure de n’importe quel serveur disponible.

> [!Note]  
> Les handles automatiques ne sont pas pris en charge pour la plateforme Macintosh.

 

Vous spécifiez l’utilisation de handles auto en incluant l’attribut de \[ [**\_ gestion automatique**](/windows/desktop/Midl/auto-handle) \] dans le CCP. L’exemple d’horodatage utilise le ACF suivant :

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

Lorsque le ACF n’inclut aucun autre attribut de handle et que les procédures distantes n’utilisent pas de handles explicites, le compilateur MIDL utilise des handles automatiques par défaut. Il utilise également des handles automatiques comme valeur par défaut lorsque le ACF n’est pas présent.

Les procédures distantes sont spécifiées dans le fichier IDL. Le descripteur automatique ne doit pas apparaître en tant qu’argument de la procédure distante. Par exemple :

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

L’avantage du descripteur automatique est que le développeur n’a pas besoin d’écrire du code pour gérer le descripteur ; les stubs gèrent automatiquement la liaison. Cela est très différent de l' [exemple Hello, World](tutorial.md), où le client gère le handle primitif implicite défini dans le ACF et doit appeler plusieurs fonctions runtime pour établir le handle de liaison.

 

 