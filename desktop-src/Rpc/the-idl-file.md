---
title: Fichier IDL
description: Le fichier IDL se compose d’une ou de plusieurs définitions d’interface, chacune ayant un en-tête et un corps.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416578"
---
# <a name="the-idl-file"></a>Fichier IDL

Le fichier IDL se compose d’une ou de plusieurs définitions d’interface, chacune ayant un en-tête et un corps. L’en-tête contient des informations qui s’appliquent à l’ensemble de l’interface, telles que l’UUID. Ces informations sont placées entre crochets et sont suivies de l' **interface** du mot clé et du nom de l’interface. Le corps contient des définitions de type de données de style C et des prototypes de fonction, complétés par des attributs qui décrivent comment les données sont transmises sur le réseau.

Dans cet exemple, l’en-tête d’interface contient uniquement l’UUID et le numéro de version. Le numéro de version garantit qu’en présence de plusieurs versions d’une interface RPC, seules les versions compatibles du client et du serveur seront connectées.

Le corps de l’interface contient le prototype de fonction pour **HelloProc**. Dans ce prototype, le paramètre de fonction pszString a les attributs **\[** [**dans**](/windows/desktop/Midl/in) **\]** et **\[** [**String**](/windows/desktop/Midl/string) **\]** . L’attribut **\[ in \]** indique à la bibliothèque Runtime que le paramètre est passé uniquement du client au serveur. L’attribut **\[ String \]** spécifie que le stub doit traiter le paramètre comme une chaîne de caractères de style C.

L’application cliente doit être en mesure d’arrêter l’application serveur. par conséquent, l’interface contient un prototype pour une autre fonction à distance,**Shutdown** , qui sera implémentée plus tard dans ce didacticiel.

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 