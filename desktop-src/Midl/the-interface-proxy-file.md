---
title: Fichier de proxy d’interface
description: Le fichier de proxy d’interface (U \_ p. c) est un fichier c qui contient des routines équivalentes à celles du stub client et des fichiers stub du serveur d’une interface d’objet (com).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL et COM MIDL, interfaces, fichiers proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093134"
---
# <a name="the-interface-proxy-file"></a>Fichier de proxy d’interface

Le fichier de proxy d’interface (U \_ p. c) est un fichier c qui contient des routines équivalentes à celles du stub client et des fichiers stub du serveur d’une interface d’objet (com). Ce fichier contient des implémentations des routines de substitution pour le client et le serveur dans le mode inline du compilateur ou des données équivalentes et des thunks dans les modes interprétés, ainsi que d’autres données de collage COM appropriées, telles que les vtables proxy et stub.

Le fichier proxy d’interface comprend les routines et les données de prise en charge uniquement pour les méthodes des interfaces définies dans le fichier IDL actuel. Pour clarifier ce comportement, un exemple étendu est utilisé tout au long de cette section. Lors de la compilation d’un fichier IDL avec une interface telle que IFaceB qui hérite de IFaceA, les données et routines auxiliaires associées à IFaceB sont générées dans le fichier proxy actuel, tandis que l’interface de base IFaceA les données auxiliaires et les routines connexes se trouvent dans le proxy généré à partir du fichier IDL contenant la définition IFaceA. Le compilateur génère toutes les données nécessaires pour identifier les substituts de l’interface de base et les déléguer quand cela est nécessaire pour prendre en charge les méthodes IFaceA utilisées par le biais de l’interface IFaceB.

Pour chaque méthode d’une interface dans le fichier IDL actuel, le fichier proxy contient les deux méthodes de substitution suivantes lorsqu’elles sont compilées en mode mixte ([/OS](-os.md)), et les données d’interpréteur équivalentes lorsqu’elles sont compilées en mode interpréteur ([/OI](-oi.md)).

-   Le substitut côté client, tel que la \_ méthode IFaceB \_ proxy dans cet exemple.

    Ce substitut côté client est le point d’entrée virtuel sur lequel le client, par exemple IFaceB :: Method, est distribué. Il marshale les arguments d’entrée dans un formulaire transmissible, transmet les arguments marshalés ainsi que les informations qui identifient l’interface et l’opération, puis démarshale la valeur de retour et tous les arguments de sortie lors du retour de l’opération appelée.

-   Substitut côté serveur, par exemple, \_ stub de méthode IFaceB \_ .

    Ce substitut côté serveur est le point d’entrée virtuel sur lequel le runtime sous-jacent distribue sur le serveur pour émuler le client. Elle démarshale les arguments d’entrée pour répliquer les données du client, appelle l’implémentation du serveur de la fonction d’interface, puis marshale et transmet la valeur de retour et tous les arguments de sortie au côté client.

Le nom par défaut d’un fichier proxy généré à partir d’un fichier. idl est le fichier \_ p. c. Utilisez le commutateur du compilateur [**/proxy**](-proxy.md) MIDL pour remplacer le nom par défaut du fichier de proxy d’interface. Les commutateurs [**/env**](-env.md) et [**/out**](-out.md) affectent ce fichier.

 

 




