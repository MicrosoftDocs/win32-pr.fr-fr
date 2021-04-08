---
description: Après avoir sélectionné le CIEM approprié pour la validation, un développeur doit rassembler les actions personnalisées dans une base de données ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Génération d’une base de données ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864426"
---
# <a name="building-an-ice-database"></a>Génération d’une base de données ICE

Après avoir sélectionné le [CIEM](internal-consistency-evaluators-ices.md) approprié pour la validation, un développeur doit rassembler les actions personnalisées dans une base de données Ice. Un fichier. CUB est une base de données. msi standard qui contient uniquement le CIEM et les tables requises. Un fichier. CUB ne peut pas être installé et est utilisé uniquement pour stocker et fournir l’accès aux actions personnalisées ICE.

Un fichier. CUB contient les tables de base de données suivantes.



| Table de charge de travail                                  | Description                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Binaire](binary-table.md)             | Fichiers de script, dll et exe des actions en douane ICE qui sont référencées dans la table CustomAction.                                                                                                                                                                 |
| [CustomAction](customaction-table.md) | Chaque enregistrement dans cette table correspond à une action personnalisée ICE incluse dans le fichier. CUB.                                                                                                                                                                                   |
| \_ICESequence                          | Ce tableau répertorie les actions de la glace en douane incluses dans le fichier. CUB dans leur séquence d’exécution. Les actions personnalisées ICE répertoriées dans ce tableau sont exécutées en appelant [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), ou exécutées individuellement à l’aide de [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). |
| [\_Validation](-validation-table.md)  | Cette table contient les entrées du fichier. CUB qui doivent être fusionnées dans la \_ table de validation.                                                                                                                                                                               |
| \_Spécial                              | Toutes les tables de traitement spéciales requises par certaines actions personnalisées ICE doivent être incluses dans le fichier. CUB. Le nom de ces tables doit avoir un trait de soulignement de début.                                                                                                        |



 

Consultez [exemple de fichier. CUB](sample--cub-file.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération d’une glace](building-an-ice.md)
</dt> </dl>

 

 



