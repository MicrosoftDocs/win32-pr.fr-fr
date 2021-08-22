---
title: Handles de liaison
description: La liaison est le processus de création d’une connexion logique entre un programme client et un programme serveur. Les informations qui composent la liaison entre le client et le serveur sont représentées par une structure appelée descripteur de liaison.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09eae434fde790531a6f723cab6dc0b0613ee2fc99d680478d697cb550d6a18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932339"
---
# <a name="binding-handles"></a>Handles de liaison

La liaison est le processus de création d’une connexion logique entre un programme client et un programme serveur. Les informations qui composent la liaison entre le client et le serveur sont représentées par une structure appelée descripteur de liaison.

Un handle de liaison est analogue à un descripteur de fichier retourné par la fonction de la bibliothèque Runtime C fopen, ou un handle de fenêtre retourné par la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .

Comme avec ces handles, votre application ne peut pas accéder directement aux informations contenues dans le handle de liaison et les manipuler. Les informations contenues dans une structure de données de handle de liaison sont uniquement disponibles pour les bibliothèques Runtime RPC. Vous fournissez le descripteur, les bibliothèques Runtime accèdent aux données appropriées et les manipulent.

Cette section présente une discussion sur les descripteurs de liaison dans les rubriques suivantes :

-   [Types de handles de liaison](types-of-binding-handles.md)
-   [Liaison côté client](client-side-binding.md)
-   [Liaison côté serveur](server-side-binding.md)
-   [Handles entièrement et partiellement liés](fully-and-partially-bound-handles.md)
-   [Interprétation des informations de liaison](interpreting-binding-information.md)
-   [Extensions de Binding-Handle Microsoft RPC](microsoft-rpc-binding-handle-extensions.md)
-   [Fonctions de gestion de liaison](binding-handle-functions.md)
-   [La base de données du service de noms RPC](the-rpc-name-service-database.md)

 

 