---
title: Interfaces DirectML
description: Les interfaces suivantes sont déclarées dans DirectML. h.
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: deb388962043926afd3868785364df6297b05d78f3997359fc88ea97ab679f33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728949"
---
# <a name="directml-interfaces"></a>Interfaces DirectML

Les interfaces suivantes sont déclarées dans DirectML. h.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | Crée un appareil DirectML pour un appareil Direct3D 12 donné. |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | Enregistre les distributions de DirectML dans une liste de commandes Direct3D 12. |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | Représente une forme compilée et efficace d’un opérateur apte à être exécuté sur le GPU. |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | Contrôle la couche de débogage DirectML. |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | Représente un appareil DirectML, utilisé pour créer des opérateurs, des tables de liaison, des enregistreurs de commande et d’autres objets. |
| [**IDMLDevice1**](/windows/desktop/api/directml/nn-directml-idmldevice1) | Représente un appareil DirectML, utilisé pour créer des opérateurs, des tables de liaison, des enregistreurs de commande et d’autres objets. |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | Interface implémentée par tous les objets créés à partir de l’appareil DirectML. |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | Implémenté par des objets qui peuvent être enregistrés dans une liste de commandes pour la distribution sur le GPU, à l’aide de [IDMLCommandRecorder :: RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch). |
| [**IDMLObject**](/windows/desktop/api/directml/nn-directml-idmlobject) | Interface à partir de laquelle [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice) et [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild) héritent directement (et toutes les autres interfaces, indirectement). Par conséquent, il fournit des méthodes communes à toutes les interfaces DirectML, notamment les méthodes pour associer des données privées et annoter les noms d’objets. |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | Représente un opérateur DirectML. |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | Représente un objet spécialisé dont l’objectif est d’initialiser les opérateurs compilés. |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | Implémentée par des objets qui peuvent être supprimés de la mémoire GPU et, par conséquent, qui peuvent être fournis à [IDMLDevice :: expulsion](/windows/desktop/api/directml/nf-directml-idmldevice-evict) et [IDMLDevice :: MakeResident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident). |

## <a name="related-topics"></a>Rubriques connexes

* [Référence DirectML](direct3d-directml-reference.md)
* [Référence de base](direct3d-12-core-reference.md)
* [Référence de Direct3D 12](direct3d-12-reference.md)
