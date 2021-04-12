---
description: Un fournisseur de services multimédias doit implémenter un sous-ensemble minimal d’interfaces MSPI ITMSPAddress ITTerminalSupport ITStreamControl et ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Écriture d’un fournisseur de services multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321442"
---
# <a name="writing-a-media-service-provider"></a><span data-ttu-id="bdb8c-103">Écriture d’un fournisseur de services multimédia</span><span class="sxs-lookup"><span data-stu-id="bdb8c-103">Writing a Media Service Provider</span></span>

<span data-ttu-id="bdb8c-104">Un fournisseur de services multimédias doit implémenter un sous-ensemble minimal d’interfaces MSPI : [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)et [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="bdb8c-104">A media service provider must implement a minimum subset of MSPI interfaces: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span> <span data-ttu-id="bdb8c-105">La prise en charge des sous-flux est facultative.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-105">SubStream support is optional.</span></span> <span data-ttu-id="bdb8c-106">En outre, un MSP donné peut implémenter des méthodes supplémentaires, telles que les contrôles requis pour le matériel spécialisé.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-106">In addition, a given MSP may implement additional methods, such as controls required for specialized hardware.</span></span>

<span data-ttu-id="bdb8c-107">Les documents matériels suivants :</span><span class="sxs-lookup"><span data-stu-id="bdb8c-107">The following material documents:</span></span>

-   <span data-ttu-id="bdb8c-108">Les [classes de base TAPI 3 MSP](tapi-3-msp-base-classes.md), qui sont un ensemble de classes C++ conçues pour simplifier la tâche de création d’un MSP basé sur DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-108">The [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md), which are a set of C++ classes designed to simplify the task of building a DirectShow-based MSP.</span></span> <span data-ttu-id="bdb8c-109">Les classes de base implémentent toutes les interfaces MSPI de manière générique.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-109">The base classes implement all the MSPI interfaces in a generic manner.</span></span> <span data-ttu-id="bdb8c-110">Les différents MSP peuvent remplacer les fonctions propres à MSP et fournir leurs propres implémentations.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-110">Different MSPs can override MSP-specific functions and provide their own implementations.</span></span>
-   <span data-ttu-id="bdb8c-111">Le [Gestionnaire de terminal TAPI 3](tapi-3-terminal-manager.md), qui fournit des interfaces et des méthodes utilisées par un MSP pour contrôler les terminaux.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-111">The [TAPI 3 Terminal Manager](tapi-3-terminal-manager.md), which provides interfaces and methods used by an MSP to control terminals.</span></span>
-   <span data-ttu-id="bdb8c-112">[Terminaux enfichables](writing-a-pluggable-terminal.md), qui permettent à une application plutôt qu’à un MSP de créer des terminaux.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-112">[Pluggable Terminals](writing-a-pluggable-terminal.md), which allow an application instead of an MSP to create terminals.</span></span> <span data-ttu-id="bdb8c-113">Les développeurs qui ont déjà été expérimentés chez l’écriture de fournisseurs de services seront les créateurs principaux de terminaux enfichables.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-113">Developers who are already experienced at writing service providers will be the primary creators of pluggable terminals.</span></span> <span data-ttu-id="bdb8c-114">La version initiale mise en œuvre pour cette version est destinée aux applications de serveur de conférence qui doivent ajouter des clients non-Windows 2000 ou non multicast à des conférences de multidiffusion SDP/IP multifournisseurs TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-114">The initial version implemented for this release is aimed at conferencing server applications that need to add non-Windows 2000 or non-multicast clients to TAPI 3 multi-party SDP/IP multicast conferences.</span></span>

 

 
