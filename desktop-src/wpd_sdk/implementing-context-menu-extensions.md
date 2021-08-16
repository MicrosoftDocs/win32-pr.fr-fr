---
description: Implémentation des extensions de menu contextuel
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implémentation des extensions de menu contextuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090f37b4cf77f9508e8c149ef6389297c561e1a4e574ef767f3a5e5c7e07fe05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194682"
---
# <a name="implementing-context-menu-extensions"></a>Implémentation des extensions de menu contextuel

L’extension d’espace de noms WPD prend en charge les menus contextuels (ou raccourcis) extensibles. Voici les menus qui s’affichent lorsqu’un utilisateur clique avec le bouton droit sur un objet tel qu’un fichier ou un dossier. Certaines applications WPD tirent parti de ces menus extensibles pour prendre en charge les opérations sur le contenu côté appareil (ou les objets qui résident sur l’appareil).

Les menus contextuels extensibles sont pris en charge par les interfaces décrites dans le tableau suivant. pour plus d’informations sur l’une de ces interfaces, consultez le SDK Windows.



| Interface           | Description                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| IContextMenu        | le Shell Windows Vista appelle les méthodes dans cette interface pour créer ou fusionner le nouveau menu contextuel avec l’objet donné. |
| IDataObject         | Utilisé pour passer le tableau PIDL du menu contextuel au gestionnaire de menu contextuel.                                                    |
| IPropertySetStorage | Cette interface est utilisée pour récupérer les propriétés WPD pour l’objet donné.                                                    |
| IPropertyStorage    | Cette interface est également utilisée pour récupérer les propriétés WPD pour l’objet donné.                                               |
| IShellExtInit       | initialise les extensions de l’interpréteur de commandes Windows Vista pour le menu contextuel.                                                       |
| IStream             | À fournir.                                                                                                            |



 

les menus contextuels pour les api WPD sont implémentés comme n’importe quel autre menu contextuel dans Windows Vista. Si vous avez déjà implémenté un gestionnaire de menu contextuel, vous pouvez modifier votre code existant afin qu’il prenne en charge le contenu côté appareil. si vous n’avez jamais créé de gestionnaire de menu contextuel, consultez la rubrique création de gestionnaires de menu contextuel dans la SDK Windows.

Les deux points auxquels un gestionnaire de menu contextuel WPD diffère de tout autre gestionnaire se trouvent dans l’inscription du gestionnaire et la prise en charge du contenu côté appareil.

 

 



