---
description: Les événements WMI sont remis par le fournisseur d’événements à un consommateur temporaire ou permanent. Le système d’événements WMI utilise la comparaison des descripteurs de sécurité sur les événements et les SID de compte d’utilisateur pour contrôler l’accès aux événements.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Sécurisation des événements WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202165"
---
# <a name="securing-wmi-events"></a><span data-ttu-id="d3fee-104">Sécurisation des événements WMI</span><span class="sxs-lookup"><span data-stu-id="d3fee-104">Securing WMI Events</span></span>

<span data-ttu-id="d3fee-105">Les événements WMI sont remis par le [*fournisseur d’événements*](gloss-e.md) à un consommateur [*temporaire*](gloss-t.md) ou [*permanent*](gloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="d3fee-105">WMI events are delivered by the [*event provider*](gloss-e.md) to a [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md) consumer.</span></span> <span data-ttu-id="d3fee-106">Le système d’événements WMI utilise la comparaison des [*descripteurs de sécurité*](gloss-s.md) sur les événements et les [*sid*](gloss-s.md) de compte d’utilisateur pour contrôler l’accès aux événements.</span><span class="sxs-lookup"><span data-stu-id="d3fee-106">The WMI event system uses the comparison of [*security descriptors*](gloss-s.md) on events and user account [*SIDs*](gloss-s.md) to control event access.</span></span>

<span data-ttu-id="d3fee-107">Les événements sont remis sous la forme d’une instance d’une classe d’événements généralement, mais pas nécessairement, dérivée en fin d' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="d3fee-107">Events are delivered in the form of an instance of an event class usually, but not necessarily, derived ultimately from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="d3fee-108">WMI fournit plusieurs classes d’événements générales dans les [classes système WMI](wmi-system-classes.md), telles que [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md).</span><span class="sxs-lookup"><span data-stu-id="d3fee-108">WMI supplies several general event classes in the [WMI System Classes](wmi-system-classes.md), such as [**\_\_InstanceModificationEvent**](--instancemodificationevent.md).</span></span> <span data-ttu-id="d3fee-109">Les fournisseurs peuvent également fournir leurs propres classes d’événements.</span><span class="sxs-lookup"><span data-stu-id="d3fee-109">Providers may also supply their own event classes.</span></span> <span data-ttu-id="d3fee-110">Par exemple, le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) a des classes d’événements qui signalent la modification d’une clé ou d’une valeur de Registre, par exemple [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="d3fee-110">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) has event classes that report the change of a registry key or value, such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="d3fee-111">Les rubriques suivantes fournissent des informations sur la sécurisation de la remise des événements pour les fournisseurs et la réception sécurisée des événements pour les applications et les scripts clients :</span><span class="sxs-lookup"><span data-stu-id="d3fee-111">The following topics supply information about securing delivery of events for providers and receiving events securely for client scripts and applications:</span></span>

-   [<span data-ttu-id="d3fee-112">Fournir des événements en toute sécurité</span><span class="sxs-lookup"><span data-stu-id="d3fee-112">Providing Events Securely</span></span>](providing-events-securely.md)
-   [<span data-ttu-id="d3fee-113">Réception des événements en toute sécurité</span><span class="sxs-lookup"><span data-stu-id="d3fee-113">Receiving Events Securely</span></span>](receiving-events-securely.md)

## <a name="related-topics"></a><span data-ttu-id="d3fee-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3fee-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3fee-115">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="d3fee-115">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
