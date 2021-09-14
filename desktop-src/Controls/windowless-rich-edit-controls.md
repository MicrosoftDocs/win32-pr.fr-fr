---
title: Contrôles RichEdit sans fenêtre
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles RichEdit sans fenêtre.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115198"
---
# <a name="windowless-rich-edit-controls"></a>Contrôles RichEdit sans fenêtre

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles RichEdit sans fenêtre. Le modèle COM (Component Object Model) définit un jeu d’interfaces pour prendre en charge les objets sans fenêtre. Les objets sans fenêtre peuvent accéder à l’état actif sur place sans avoir leur propre fenêtre, mais plutôt utiliser la fenêtre de leur conteneur. Par conséquent, un objet sans fenêtre utilise moins de ressources système et offre de meilleures performances via une activation et une désactivation plus rapides. En outre, les objets sans fenêtre peuvent être non rectangulaires et transparents.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                                                          | Contenu                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos des contrôles RichEdit sans fenêtre](about-windowless-rich-edit-controls.md) | Un contrôle RichEdit sans fenêtre, également connu sous le nom d’objet de services de texte, est un objet qui fournit les fonctionnalités d’un [contrôle RichEdit](rich-edit-controls.md) sans fournir la fenêtre.<br/> |



 

### <a name="functions"></a>Fonctions



| Rubrique                                            | Contenu                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | La fonction [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) crée une instance d’un objet de services de texte. L’objet services de texte prend en charge une variété d’interfaces, notamment [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) et le modèle d’objet de texte (Tom).<br/> |



 

### <a name="interfaces"></a>Interfaces



| Rubrique                                  | Contenu                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | L’interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) est utilisée par un objet Text services pour obtenir des services d’hôte de texte.<br/> |
| [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) | Étend TOM pour fournir des fonctionnalités supplémentaires pour une opération sans fenêtre.<br/>                                     |



 

 

 





