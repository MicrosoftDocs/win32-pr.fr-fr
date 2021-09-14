---
title: Stub client
description: Le module stub client fournit des points d’entrée de substitution sur le client pour chacune des opérations définies dans le fichier IDL d’entrée.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL et RPC MIDL, interfaces, stub client
- interfaces MIDL
- interfaces MIDL, MIDL et RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093142"
---
# <a name="the-client-stub"></a>Stub client

Le module stub client fournit des points d’entrée de substitution sur le client pour chacune des opérations définies dans le fichier IDL d’entrée.

Lorsque l’application cliente effectue un appel à la procédure distante, son appel passe tout d’abord à la routine de substitution dans le fichier stub client. La routine stub cliente exécute les fonctions suivantes :

-   Marshale les arguments. Le stub client empaquette des arguments d’entrée dans un format qui peut être transmis au serveur.
-   Appelle la bibliothèque Runtime du client pour transmettre des arguments à l’espace d’adressage distant et appelle la procédure distante dans l’espace d’adressage du serveur.
-   Démarshale les arguments de sortie. Le stub client décompresse les arguments de sortie et retourne à l’appelant.

Le compilateur MIDL bascule [**/client**](-client.md), [**/cstub**](-cstub.md)et [**/out**](-out.md) sur le fichier stub client.

 

 




