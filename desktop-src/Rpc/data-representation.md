---
title: Représentation des données
description: Les environnements informatiques peuvent varier considérablement, comme les architectures réseau.
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- Appel de procédure distante RPC, description, représentation des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4de187f2b646e55cd4f1a269f0504a2d43e951c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229182"
---
# <a name="data-representation"></a>Représentation des données

Les environnements informatiques peuvent varier considérablement, comme les architectures réseau. Pour prendre en compte ces différences, MIDL vous permet de modifier la façon dont vous représentez les données. Vous pouvez parfois simplifier le développement en convertissant les données dans un format que votre application peut gérer plus facilement. Vous pouvez modifier le format de données de votre application afin qu’elle puisse être transmise plus efficacement sur le réseau.

Les **\[** attributs [**transmit \_ As**](/windows/desktop/Midl/transmit-as) **\]** et **\[** [**dereprésente \_ As**](/windows/desktop/Midl/represent-as) **\]** indiquent au compilateur d’associer un type transmissible que le stub passe entre le client et le serveur, avec un type d’utilisateur utilisé par les applications client et serveur. Vous devez fournir les routines qui effectuent la conversion entre le type d’utilisateur et le type transmissible, et les routines pour libérer la mémoire utilisée pour stocker les données converties. L’utilisation de l’attribut **\[ transmettez \_ en tant que \]** IDL ou de l’attribut de **\[ représentation \_ sous forme \]** de CCP indique au stub d’appeler ces routines de conversion avant et après la transmission. L' **\[** attribut [**transmettre \_ en tant que**](/windows/desktop/Midl/transmit-as) **\]** vous permet de convertir un type de données en un autre type de données pour la transmission sur le réseau. L' **\[** attribut [**dereprésente \_ comme**](/windows/desktop/Midl/represent-as) **\]** attribut vous permet de contrôler la façon dont les données du réseau sont présentées à l’application.

Les attributs de marshaling de **\[** [**câble \_**](/windows/desktop/Midl/wire-marshal) **\]** et **\[** d' [**utilisateur \_**](/windows/desktop/Midl/user-marshal) **\]** sont des extensions Microsoft de l’IDL OSF-DCE. Leur syntaxe et leurs fonctionnalités sont similaires à celles de la fonction de **\[ transmission \_ en \] tant** que spécifiée par DCE, respectivement, et **\[ représentent \_ \]** les attributs. La différence est que, au lieu de convertir les données d’un type en un autre, vous devez marshaler les données directement. Pour ce faire, vous devez fournir les routines externes pour le dimensionnement du tampon de données côté client et serveur, en marshalant et en démarshalant les données côté client et serveur, et en libérant les données côté serveur. Le compilateur MIDL génère des codes de format qui indiquent au moteur de NDR d’appeler ces routines externes si nécessaire.

Les attributs du marshaleur de **\[ câble \_ \]** et du **\[ \_ Marshal \] d’utilisateur** permettent de marshaler les types de données qui, autrement, ne peuvent pas être transmis entre les limites du processus. En outre, étant donné qu’il y a moins de surcharge associée à la conversion de type, le **\[ \_ Marshal \] de câble** et le **\[ \_ Marshal \] d’utilisateur** fournissent des performances améliorées au moment de l’exécution, par rapport à la **\[ transmission \_ en tant que \]** et **\[ représentent \_ comme \]**. Les attributs du **\[ \_ marshaleur \] de câble** et du **\[ \_ Marshal \] d’utilisateur** sont mutuellement exclusifs entre eux et en ce qui concerne la **\[ transmission \_ en tant \]** que et **\[ représentent \_ \]** les attributs d’un type donné.

Il est important de noter que l’implémentation des attributs de marshaling de **\[ câble \_ \]** et de **\[ \_ Marshal \] d’utilisateur** doit suivre les règles de marshaling dictées par la spécification OSF-DCE. Pour cette raison, l’utilisation de ces attributs n’est pas recommandée si vous n’êtes pas familiarisé avec le protocole câble. Vous trouverez plus d’informations sur le transfert de syntaxe NDR sur [www.Opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).

Cette section fournit une brève vue d’ensemble de ces attributs pour les attributs MIDL, dans les rubriques suivantes :

-   [**Les \_ attributs transmit As et dereprésente \_ As**](the-transmit-as-and-represent-as-attributes.md)
-   [**Attributs du marshaleur \_ de câble et du Marshal d’utilisateur \_**](the-wire-marshal-and-user-marshal-attributes.md)

 

 