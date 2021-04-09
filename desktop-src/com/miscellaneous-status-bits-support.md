---
title: Prise en charge des bits d’État divers
description: Prise en charge des bits d’État divers
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c281b52283796d67c476e8ee00383436bc2235a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028530"
---
# <a name="miscellaneous-status-bits-support"></a>Prise en charge des bits d’État divers

Les conteneurs de contrôles ActiveX doivent reconnaître et prendre en charge les bits d’État OLEMISC suivants \_ .



| Bit d’État                           | Requis ?      | Commentaires                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVATEWHENVISIBLE<br/>       | Oui<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTIVATEWHENVISIBLE<br/> | Non<br/>  | Nécessaire pour la prise en charge des contrôles inactifs et sans fenêtre. Le bit IGNOREACTIVATEWHENVISIBLE est destiné aux conteneurs hébergeant des contrôles inactifs et sans fenêtre. Le bit IGNOREACTIVATEWHENVISIBLE est introduit dans le cadre de la spécification des contrôles ActiveX 96. pour plus d’informations, consultez cette documentation.<br/> |
| INSIDEOUT<br/>                 | Non<br/>  | Il n’est généralement pas utilisé avec les contrôles ActiveX, mais plutôt avec les incorporations de documents composés. Notez que cela est contraire à la documentation du kit de développement logiciel (SDK) qui indique que ce bit doit être défini pour que le bit ACTIVATEWHENVISIBLE soit défini.<br/>                                                                             |
| INVISIBLEATRUNTIME<br/>        | Oui<br/> | Désigne un contrôle qui doit être visible au moment du design, mais invisible au moment de l’exécution.<br/>                                                                                                                                                                                                       |
| ALWAYSRUN<br/>                 | Oui<br/> |                                                                                                                                                                                                                                                                                                         |
| ACTSLIKEBUTTON<br/>            | Non<br/>  | La prise en charge est normalement obligatoire, bien qu’elle ne soit pas nécessaire pour les conteneurs de style de document.<br/>                                                                                                                                                                                                    |
| ACTSLIKELABEL<br/>             | Non<br/>  | La prise en charge est normalement obligatoire, bien qu’elle ne soit pas nécessaire pour les conteneurs de style de document.<br/>                                                                                                                                                                                                    |
| NOUIACTIVATE<br/>              | Oui<br/> |                                                                                                                                                                                                                                                                                                         |
| ALIGNEMENT<br/>                 | Non<br/>  |                                                                                                                                                                                                                                                                                                         |
| SIMPLEFRAME<br/>               | Non<br/>  | Voir [relation contenant-contenu de site à cadre simple](simple-frame-site-containment.md)<br/>                                                                                                                                                                                                                       |
| SETCLIENTSITEFIRST<br/>        | Non<br/>  | La prise en charge de ce bit est recommandée, mais pas obligatoire.<br/>                                                                                                                                                                                                                                       |
| IMEMODE<br/>                   | Non<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

 





