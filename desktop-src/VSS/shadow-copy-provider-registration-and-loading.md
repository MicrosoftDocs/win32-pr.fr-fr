---
description: Inscription et chargement du fournisseur de clichés instantanés
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Inscription et chargement du fournisseur de clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbb239303884314375ec865e3862d6a65af7de27bd7351a74e92604d06876bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998109"
---
# <a name="shadow-copy-provider-registration-and-loading"></a>Inscription et chargement du fournisseur de clichés instantanés

## <a name="provider-registration"></a>Inscription du fournisseur

Seuls les fournisseurs d’appels VSS. Le fournisseur s’inscrit aux appels en appelant [**IVssAdmin :: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), en passant **le \_ \_ matériel de preuve VSS** pour le paramètre *eProviderType* . Une fois inscrit, le fournisseur est impliqué dans la gestion des clichés instantanés jusqu’à annulation de l’inscription à l’aide de [**IVssAdmin :: UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).

## <a name="provider-loading-and-unloading"></a>Chargement et déchargement du fournisseur

Les fournisseurs peuvent être souvent chargés et déchargés. Les fournisseurs peuvent implémenter [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) pour déterminer le moment où VSS charge ou décharge le fournisseur.

 

 



