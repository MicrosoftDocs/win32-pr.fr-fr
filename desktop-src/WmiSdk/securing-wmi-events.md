---
description: Les événements WMI sont remis par le fournisseur d’événements à un consommateur temporaire ou permanent. Le système d’événements WMI utilise la comparaison des descripteurs de sécurité sur les événements et les SID de compte d’utilisateur pour contrôler l’accès aux événements.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Sécurisation des événements WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918787"
---
# <a name="securing-wmi-events"></a>Sécurisation des événements WMI

Les événements WMI sont remis par le [*fournisseur d’événements*](gloss-e.md) à un consommateur [*temporaire*](gloss-t.md) ou [*permanent*](gloss-p.md) . Le système d’événements WMI utilise la comparaison des [*descripteurs de sécurité*](gloss-s.md) sur les événements et les [*sid*](gloss-s.md) de compte d’utilisateur pour contrôler l’accès aux événements.

Les événements sont remis sous la forme d’une instance d’une classe d’événements généralement, mais pas nécessairement, dérivée en fin d' [**\_ \_ événement**](--event.md). WMI fournit plusieurs classes d’événements générales dans les [classes système WMI](wmi-system-classes.md), telles que [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md). Les fournisseurs peuvent également fournir leurs propres classes d’événements. Par exemple, le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) a des classes d’événements qui signalent la modification d’une clé ou d’une valeur de Registre, par exemple [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

Les rubriques suivantes fournissent des informations sur la sécurisation de la remise des événements pour les fournisseurs et la réception sécurisée des événements pour les applications et les scripts clients :

-   [Fournir des événements en toute sécurité](providing-events-securely.md)
-   [Réception des événements en toute sécurité](receiving-events-securely.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 
