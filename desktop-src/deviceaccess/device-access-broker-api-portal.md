---
title: API d’accès aux appareils
description: utilisez l’API d’accès à l’appareil pour écrire Windows stocker des applications d’appareil pour des appareils spécialisés qui utilisent des pilotes personnalisés.
ms.assetid: 51329746-291e-4ac6-9029-ebe4727d5d7d
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 72b9340c157e54f85145a03852712c826b71bd49cffb50ae2a4e5fe20e660246
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029069"
---
# <a name="device-access-api"></a>API d’accès aux appareils

## <a name="purpose"></a>Objectif

vous pouvez utiliser l’API d’accès à l’appareil pour écrire Windows stocker des applications d’appareil pour des appareils spécialisés qui utilisent des pilotes personnalisés. L’API fournit des méthodes pour envoyer des codes de contrôle afin de communiquer avec le pilote personnalisé de l’appareil.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|---|---|
| [À propos de l’API d’accès aux appareils](about-the-device-access-api.md)<br/> | l’API d’accès aux appareils est destinée aux développeurs C++ qui créent une application Windows Store pour interagir avec des appareils spécialisés dans Windows 8. Cette rubrique décrit les scénarios auxquels s’applique l’API d’accès à l’appareil. elle explique également comment l’API d’accès aux appareils applique des règles de sécurité pour les applications Windows Store dans Windows 8.<br/> |
| [Comment utiliser l’API d’accès à l’appareil](using-the-device-access-api.md)<br/> | Cette rubrique contient des tâches et des considérations relatives à la conception pour l’utilisation de l’API d’accès aux appareils.<br/> |
| [Informations de référence sur la programmation C++ de l’API d’accès aux appareils](device-access-api-c---programming-reference.md)<br/> | Fournit des pages de référence pour les fonctions et les interfaces dans l’API d’accès à l’appareil.<br/> |
| [Glossaire de l’accès aux appareils](deviceaccess-glossary.md)<br/> | Voici les termes utilisés dans la documentation de l’API d’accès aux appareils.<br/> |
| [Autres API](other-apis.md)<br/> | Ces interfaces ne sont pas prises en charge et ne doivent pas être utilisées. Utilisez plutôt les API dans la [référence de programmation C++ de l’API d’accès à l’appareil](device-access-api-c---programming-reference.md) .<br/> |

## <a name="developer-audience"></a>Développeurs concernés

L’API d’accès aux appareils est conçue pour les fabricants de matériel indépendants et les développeurs OEM qui connaissent C++ et le modèle COM (Component Object Model).

## <a name="related-topics"></a>Rubriques connexes

[exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications de l’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)
