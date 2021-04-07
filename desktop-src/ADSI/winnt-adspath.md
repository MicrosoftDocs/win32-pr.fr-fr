---
title: ADsPath de Winnt
description: Cette rubrique contient des exemples de chaînes à utiliser pour la valeur ADsPath de Winnt.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- Fournisseur de services Winnt ADSI, Winnt ADsPath
- ADsPath ADSI, WinNT, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea2c3db1b5234fb07045d921858766a105c4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939566"
---
# <a name="winnt-adspath"></a>ADsPath de Winnt

La chaîne ADsPath du fournisseur ADSI Winnt peut prendre l’une des formes suivantes :


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



Le nom de domaine peut être un nom NETBIOS ou un nom DNS.

Le serveur est le nom d’un serveur spécifique dans le domaine.

Le chemin d’accès correspond au chemin d’accès de l’objet, tel que « printserver1/exemple ».

Le nom de l’objet est le nom d’un objet spécifique.

La classe d’objet est le nom de classe de l’objet nommé. Voici un exemple de cette utilisation : « WinNT://MyServer/JeffSmith,user ». La spécification d’un nom de classe peut améliorer les performances de l’opération de liaison.

 

 




