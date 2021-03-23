---
title: Durée de vie et synchronisation des ressources
description: Afin d’éviter un comportement indéfini, votre application DirectML doit gérer correctement les durées de vie des objets et la synchronisation entre l’UC et le GPU.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 6e8ab30c5c87c135ef3bdac0c1bc2a3d64040787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104802"
---
# <a name="resource-lifetime-and-synchronization"></a>Durée de vie et synchronisation des ressources

Tout comme avec Direct3D 12, votre application DirectML doit (afin d’éviter un comportement indéfini) gérer correctement les durées de vie des objets et la synchronisation entre l’UC et le GPU. DirectML suit un modèle de durée de vie des ressources identique à celui de Direct3D 12.

- Les dépendances de durée de vie entre deux objets UC sont gérées par DirectML à l’aide de décomptes de références forts. Votre application n’a pas besoin de gérer manuellement les dépendances de durée de vie du processeur. Par exemple, chaque enfant d’appareil détient une référence forte à son appareil parent.
- Les dépendances de durée de vie entre les objets GPU &mdash; ou les dépendances qui couvrent le processeur et le GPU &mdash; ne sont pas gérées automatiquement. C’est la responsabilité de votre application de s’assurer que les ressources GPU se trouvent au moins jusqu’à ce que tout le travail à l’aide de cette ressource ait terminé l’exécution sur le GPU.

## <a name="directml-devices"></a>Appareils DirectML

L’appareil DirectML est un objet de fabrique sans état thread-safe. Chaque enfant d’appareil (voir [**IDMLDeviceChild**](/windows/desktop/api/directml/nn-directml-idmldevicechild)) contient une référence forte à son appareil DirectML parent (voir [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice)). Cela signifie que vous pouvez toujours récupérer l’interface d’appareil parent à partir de n’importe quelle interface enfant d’appareil.

Un appareil DirectML contient à son tour une référence forte au périphérique Direct3D 12 qui a été utilisé pour le créer (consultez [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device), et interfaces dérivées).

Étant donné que l’appareil DirectML est sans État, il est implicitement thread-safe. Vous pouvez appeler des méthodes sur l’appareil DirectML à partir de plusieurs threads simultanément, sans nécessiter de synchronisation externe.

Toutefois, contrairement à l’appareil Direct3D 12, l’appareil DirectML n’est pas un objet singleton. Vous êtes libre de créer autant d’appareils DirectML que vous le souhaitez. Toutefois, vous ne pouvez pas mélanger et faire correspondre des enfants d’appareils qui appartiennent à des appareils différents. Par exemple, [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) et [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) sont deux genres d’enfants d’appareil (les deux interfaces dérivent directement ou indirectement de **IDMLDeviceChild**). Et vous ne pouvez pas utiliser une table de liaison (**IDMLBindingTable**) pour effectuer une liaison pour un opérateur (**IDMLCompiledOperator**) si l’opérateur et la table de liaison appartiennent à différentes instances d’appareil DirectML.

Étant donné que l’appareil DirectML n’est pas un singleton, la suppression de l’appareil s’effectue en fonction de l’appareil, plutôt que d’être un événement à l’échelle du processus, comme pour un appareil Direct3D 12. Pour plus d’informations, consultez [gestion des erreurs et suppression d’appareils dans DirectML](dml-errors.md).

## <a name="lifetime-requirements-of-gpu-resources"></a>Exigences de durée de vie des ressources GPU

Comme Direct3D 12, DirectML ne se synchronise pas automatiquement entre l’UC et le GPU. elle ne conserve pas non plus automatiquement les ressources actives pendant qu’elles sont utilisées par le GPU. Au lieu de cela, il s’agit des responsabilités de votre application.

Lors de l’exécution d’une liste de commandes contenant des distributions DirectML, votre application doit s’assurer que les ressources GPU restent actives jusqu’à ce que toutes les tâches utilisant ces ressources aient terminé leur exécution sur le GPU.

Dans le cas de [**IDMLCommandRecorder :: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) pour un opérateur DirectML, qui comprend les objets suivants.

- [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) en cours d’exécution (ou [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) à la place, en cas d’initialisation d’opérateur).
- **IDMLCompiledOperator** sauvegardant la table de liaison utilisée pour lier l’opérateur.
- Objets [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) liés en tant qu’entrées/sorties de l’opérateur.
- Objets **ID3D12Resource** liés en tant que ressources persistantes et temporaires, le cas échéant.
- [**ID3D12CommandAllocator**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandallocator) sauvegardant la liste de commandes elle-même.

Toutes les interfaces DirectML ne représentent pas les ressources GPU. Par exemple, une table de liaison n’a pas besoin d’être gardée active tant que toutes les distributions qui l’utilisent n’ont *pas* été exécutées sur le GPU. Cela est dû au fait que la table de liaison elle-même ne possède aucune ressource GPU. Au lieu de cela, le tas du descripteur. Par conséquent, le *tas du descripteur* sous-jacent est l’objet qui doit rester actif jusqu’à ce que l’exécution se termine, et non la table de liaison elle-même.

Un concept similaire existe dans Direct3D 12. Un *allocateur* de commande doit rester actif jusqu’à ce que toutes les exécutions qui l’utilisent soient terminées sur le GPU. dans la mesure où elle possède la mémoire GPU. Toutefois, une *liste* de commandes ne possède pas de mémoire GPU. elle peut donc être réinitialisée ou libérée dès qu’elle a été soumise pour exécution.

Dans DirectML, les opérateurs compilés ([**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator)) et les initialiseurs d’opérateur ([**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer)) possèdent tous les deux des ressources GPU directement. ils doivent donc être maintenus actifs jusqu’à ce que toutes les distributions qui les utilisent aient terminé leur exécution sur le GPU. En outre, toute ressource Direct3D 12 utilisée (allocateurs de commandes, tas de descripteurs, mémoires tampons, par exemple) doit être conservée de la même façon que votre application.

Si vous libérez prématurément un objet alors qu’il est toujours utilisé par le GPU, le résultat est un comportement indéfini, ce qui risque de provoquer la suppression du périphérique ou d’autres erreurs.

## <a name="cpu-and-gpu-synchronization"></a>Synchronisation du processeur et du GPU

DirectML n’envoie pas lui-même de travail d’exécution sur le GPU. Au lieu de cela, la [méthode **IDMLCommandRecorder :: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) *enregistre* la distribution de ce travail dans une liste de commandes en vue d’une exécution ultérieure. Votre application doit ensuite fermer et soumettre sa liste de commandes pour exécution en appelant [**ID3D12CommandQueue :: ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists), comme avec n’importe quelle liste de commandes Direct3D 12.

Étant donné que DirectML n’envoie pas lui-même de travail d’exécution sur le GPU, il ne crée pas non plus de délimiteurs et n’exécute aucune forme de synchronisation de processeur/GPU à votre place. Il est de la responsabilité de votre application d’utiliser les primitives Direct3D 12 appropriées pour attendre la fin de l’exécution du travail soumis sur le GPU, si nécessaire. Pour plus d’informations, consultez [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) et [**ID3D12CommandQueue :: signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal).

## <a name="see-also"></a>Voir aussi

* [Exécution et synchronisation de listes de commandes](/windows/desktop/direct3d12/executing-and-synchronizing-command-lists)
* [Gestion des erreurs et suppression des appareils dans DirectML](dml-errors.md)