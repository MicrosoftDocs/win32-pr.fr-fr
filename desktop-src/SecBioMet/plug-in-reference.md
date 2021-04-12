---
title: Référence du plug-in
description: Fonctions d’adaptateur, fonctions wrapper et structures pour créer des adaptateurs de plug-in personnalisés de trois types de moteur, de capteur et de stockage.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API Windows Biometric Framework API Windows Biometric Framework, référence de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462438"
---
# <a name="plug-in-reference"></a>Référence du plug-in

Les périphériques biométriques sont fabriqués dans un large éventail de types et de configurations. Le Windows Biometric Framework incorpore une architecture extensible qui vous permet de gérer cette variété en créant des plug-ins personnalisés. Au centre de cette architecture se trouve un objet logiciel appelé unité biométrique. Vous pouvez considérer une unité biométrique comme une abstraction qui représente un périphérique biométrique pour l’infrastructure. Les composants logiciels enfichables appelés adaptateurs connectent l’unité biométrique au matériel associé. Il existe trois types d’adaptateurs que vous pouvez créer. Un adaptateur de moteur génère des modèles biométriques à partir d’exemples capturés, fait correspondre des exemples à des modèles existants et des modèles d’index. Un adaptateur de capteur encapsule un périphérique biométrique et fournit une interface standard pour configurer le capteur, capturer des échantillons et contrôler le workflow de données biométriques pour le moteur de traitement. Un adaptateur de stockage gère les bases de données de modèles.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                 | Description                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Fonctions de plug-in](plug-in-functions.md)<br/>                 | Fonctions que vous pouvez utiliser pour créer les plug-ins d’adaptateur qui composent une unité biométrique.<br/>                                                                     |
| [Structures de plug-in](plug-in-structures.md)<br/>               | Structures pour le développement d’applications clientes par l’API Windows Biometric Framework.<br/>                                                                   |
| [Fonctions wrapper de plug-in](plug-in-wrapper-functions.md)<br/> | Fonctions wrapper qui vous permettent d’appeler une fonction publique sur n’importe quel adaptateur attaché au pipeline sans acquérir manuellement un pointeur vers l’adaptateur.<br/> |



 

 

 





