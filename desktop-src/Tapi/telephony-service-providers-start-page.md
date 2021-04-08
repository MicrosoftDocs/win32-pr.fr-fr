---
description: Un fournisseur de services de téléphonie (TSP) est une bibliothèque de liens dynamiques (DLL) qui prend en charge le contrôle des appareils de communication via un ensemble de fonctions de service exportées.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Fournisseurs de services de téléphonie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868145"
---
# <a name="telephony-service-providers"></a>Fournisseurs de services de téléphonie

## <a name="purpose"></a>Objectif

Un fournisseur de services de téléphonie (TSP) est une bibliothèque de liens dynamiques (DLL) qui prend en charge le contrôle des appareils de communication via un ensemble de fonctions de service exportées. Une application TAPI utilise des commandes standardisées, TAPI transmet des informations au fournisseur de services de téléphonie et le TSP gère les commandes spécifiques qui doivent être échangées avec l’appareil.

Un TSP doit se conformer à l’interface TSPI (Telephony Service Provider Interface) pour fonctionner en tant que fournisseur de services au sein de l’environnement de téléphonie Microsoft. TSPI définit les fonctions externes exposées par un fournisseur de services de téléphonie fourni avec l’équipement de communication.

## <a name="developer-audience"></a>Développeurs concernés

Vous pouvez écrire des applications compatibles TAPI dans de nombreux langages, notamment Java, Visual Basic et C/C++. L’expérience de développement précédente avec les télécommunications ou d’autres applications de téléphonie est utile, mais pas nécessaire.

## <a name="run-time-requirements"></a>Conditions d’exécution

TSPI permet le développement de TSPs pour toutes les versions de Windows.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                | Description                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Vue d'ensemble](about-the-telephony-service-provider-tsp-.md)<br/> | Informations générales sur l’architecture et les composants de TSPI.<br/> |
| [Référence](tspi-reference.md)<br/>                           | Documentation pour les interfaces TSPI.<br/>                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de la téléphonie Microsoft](./microsoft-telephony-overview.md)
</dt> <dt>

[Fournisseurs de services de média](./media-service-providers-start-page.md)
</dt> <dt>

[TAPI 2,2](./tapi-2-2-start-page.md)
</dt> <dt>

[TAPI 3,1](./tapi-3-1-start-page.md)
</dt> </dl>

 

