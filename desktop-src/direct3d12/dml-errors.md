---
title: Gestion des erreurs et de la suppression des appareils dans DirectML
description: Cette rubrique explique comment déboguer la suppression de l’appareil DirectML et d’autres conditions d’erreur.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548540"
---
# <a name="handling-errors-and-device-removal-in-directml"></a>Gestion des erreurs et de la suppression des appareils dans DirectML

## <a name="device-removal"></a>Appareil-suppression

Si une erreur irrécupérable se produit, l’appareil DirectML peut entrer un État « appareil supprimé ». Les erreurs irrécupérables qui provoquent la suppression de l’appareil incluent une utilisation d’API non valide (pour les méthodes qui ne retournent pas de [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), une erreur de pilote, une défaillance matérielle ou des conditions de mémoire insuffisante (insuffisance).

Lorsqu’un appareil DirectML est supprimé, tous les appels de méthode sur l’appareil et tous les objets créés par ce périphérique deviennent non-OPS. Pour les méthodes qui retournent un [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), un code d’erreur [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) est retourné. Vous pouvez utiliser la [méthode **IDMLDevice :: GetDeviceRemovedReason**](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) pour vérifier si l’appareil DirectML a été supprimé et pour récupérer un code d’erreur plus détaillé.

Vous ne pouvez pas récupérer à partir de la suppression de l’appareil, sauf en libérant l’appareil affecté et tous ses enfants, puis en recréant l’appareil DirectML à partir de zéro.

L’appareil : la suppression de l’appareil Direct3D 12 sous-jacent entraîne également la suppression de l’appareil DirectML. En revanche, l'inverse n'est pas vrai. DirectML : la suppression de l’appareil ne peut pas nécessairement entraîner la suppression de l’appareil Direct3D 12 sous-jacent.

## <a name="debugging-directml-device-removal-and-other-errors"></a>Débogage de l’appareil DirectML-suppression et autres erreurs

La cause la plus courante des erreurs DirectML est l’utilisation d’API non valide. Une utilisation d’API non valide peut entraîner un **E_INVALIDARG** code d’erreur HRESULT, ou peut entraîner la suppression de l’appareil.

Nous vous recommandons vivement d’activer la [couche de débogage DirectML](dml-debug-layer.md) pendant votre développement, afin d’intercepter et de déboguer ces erreurs. La couche de débogage DirectML effectue une validation complète des paramètres de méthode et de l’utilisation des API, et émet des messages de sortie de débogage pour vous aider à effectuer le débogage.

## <a name="see-also"></a>Voir aussi

* [Utilisation de la couche de débogage DirectML](dml-debug-layer.md)
