---
title: Prise en charge des bits d’État divers
description: Prise en charge des bits d’État divers
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d491e4f9ab3e41cf42510beeeb037e3b58e80a5f02ebe8e86e8bb07f3be5cb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096919"
---
# <a name="miscellaneous-status-bits-support"></a>Prise en charge des bits d’État divers

ActiveX Les conteneurs de contrôle doivent reconnaître et prendre en charge les bits d’État OLEMISC suivants \_ .



| Bit d’État                           | Requis ?      | Commentaires                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVATEWHENVISIBLE<br/>       | Oui<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTIVATEWHENVISIBLE<br/> | Non<br/>  | Nécessaire pour la prise en charge des contrôles inactifs et sans fenêtre. Le bit IGNOREACTIVATEWHENVISIBLE est destiné aux conteneurs hébergeant des contrôles inactifs et sans fenêtre. le bit IGNOREACTIVATEWHENVISIBLE est introduit dans le cadre de la spécification ActiveX controls 96. pour plus d’informations, consultez cette documentation.<br/> |
| INSIDEOUT<br/>                 | Non<br/>  | il n’est généralement pas utilisé avec les contrôles de ActiveX, mais plutôt avec les incorporations de documents composés. Notez que cela est contraire à la documentation du kit de développement logiciel (SDK) qui indique que ce bit doit être défini pour que le bit ACTIVATEWHENVISIBLE soit défini.<br/>                                                                             |
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

 

 





