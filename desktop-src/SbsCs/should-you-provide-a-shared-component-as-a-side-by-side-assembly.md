---
description: Les fournisseurs de composants partagés doivent envisager de rendre leur composant disponible en tant qu’assembly côte à côte si un ou plusieurs des cas suivants sont vrais.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: Devez-vous fournir un composant partagé comme assembly côte à côte ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92dbd205db37c769050614c60ce4cc3637b27be9108f25b3c1c8f553851df82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141892"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a>Devez-vous fournir un composant partagé comme assembly côte à côte ?

Les fournisseurs de composants partagés doivent envisager de rendre leur composant disponible en tant qu’assembly côte à côte si une ou plusieurs des conditions suivantes sont vraies :

-   Le composant expose une interface de programmation d’applications riche qui est utilisée par de nombreuses applications. Par exemple, un composant tel que MSHTML, qui permet aux applications C et C++ d’accéder au modèle objet DHTML (Dynamic HTML).
-   Le composant est déjà partagé par plusieurs applications. Par exemple, un composant tel que COMCTL32, qui fournit aux applications un accès aux contrôles communs.
-   Le composant est un nouveau composant.
-   Le composant est un composant en mode utilisateur et non un pilote de périphérique.

Tous les composants ne sont pas un candidat approprié pour un assembly côte à côte. Un composant n’est pas un candidat approprié pour un assembly côte à côte si l’une des conditions suivantes est vraie :

-   Le composant gère la communication entre les applications. Par exemple, certaines parties de OLE32 ne constituent pas un bon assembly côte à côte, car vous ne souhaitez pas avoir deux versions différentes des parties qui coordonnent la communication entre les applications exécutées sur votre système.
-   Le composant gère un appareil physique ou virtuel pour le système. Par exemple, un pilote de périphérique pour un spouleur d’impression.

Dans certains cas, il est possible pour le développeur du composant de reconcevoir un composant existant afin de le rendre adapté à la publication en tant qu’assembly côte à côte. Pour plus d’informations, consultez [instructions relatives à la création d’assemblys côte à côte](guidelines-for-creating-side-by-side-assemblies.md).

 

 



