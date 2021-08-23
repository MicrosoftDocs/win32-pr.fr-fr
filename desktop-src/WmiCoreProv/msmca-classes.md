---
description: Ensemble de classes WMI qui exposent l’architecture de vérification automatique (MCA). La couche d’abstraction système (SAL) fournit tous les événements signalés dans la classe MSMCA. Intel Corporation développe et possède l’MCA.
ms.assetid: 4e35f871-5bce-49ed-a3e8-d2d967e6e2dc
title: Classes MSMCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0f70bead9acbbb23fe0e2115ac12f967c7908f1f0eefa16d65cd1a57947e76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641079"
---
# <a name="msmca-classes"></a>Classes MSMCA

Les classes MSMCA (Microsoft machine Check architecture) sont un ensemble de classes WMI qui exposent l’architecture de vérification automatique (MCA). La couche d’abstraction système (SAL) fournit tous les événements signalés dans la classe MSMCA. Intel Corporation développe et possède l’MCA.



| Classe                                                                               | Description                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**MSMCAEvent \_ CPUError**](msmcaevent-cpuerror.md)                                 | Représente un événement d’erreur d’UC.                                                                          |
| [**\_En-tête MSMCAEvent**](msmcaevent-header.md)                                     | Représente l’en-tête commun utilisé par toutes les classes MSMCAEvent.                                          |
| [**MSMCAEvent \_ InvalidError**](msmcaevent-invaliderror.md)                         | Représente une erreur MCA non valide d’architecture de vérification de la mémoire.                                            |
| [**MSMCAEvent \_ MemoryError**](msmcaevent-memoryerror.md)                           | Représente un événement d’erreur de mémoire MCA.                                                                  |
| [**MSMCAEvent \_ MemoryPageRemoved**](msmcaevent-memorypageremoved.md)               | Indique que le système d’exploitation a supprimé une page physique de mémoire.                                 |
| [**MSMCAEvent \_ PCIBusError**](msmcaevent-pcibuserror.md)                           | Représente une erreur MCA PCI bus.                                                                       |
| [**MSMCAEvent \_ PCIComponentError**](msmcaevent-pcicomponenterror.md)               | Représente une erreur de composant PCI MCA.                                                                 |
| [**MSMCAEvent \_ PlatformSpecificError**](msmcaevent-platformspecificerror.md)       | Représente une erreur MCA spécifique à la plateforme.                                                             |
| [**MSMCAEvent \_ SMBIOSError**](msmcaevent-smbioserror.md)                           | Représente une erreur du BIOS système MCA.                                                                   |
| [**MSMCAEvent \_ SwitchToCMCPolling**](msmcaevent-switchtocmcpolling.md)             | Indique que la gestion des vérifications d’ordinateur corrigée est basculée vers l’interrogation.                            |
| [**MSMCAEvent \_ SystemEventError**](msmcaevent-systemeventerror.md)                 | Représente une erreur de l’événement système MCA.                                                                  |
| [**MSMCAInfo**](msmcainfo.md)                                                      | Classe de base abstraite dont sont dérivées toutes les classes de données du fournisseur MCA (machine Check architecture). |
| [**\_Entrée MSMCAInfo**](msmcainfo-entry.md)                                         | Représente une entrée MCA, corrigée de la vérification de l’ordinateur (CMC) ou erreur de plateforme corrigée (CPE). |
| [**MSMCAInfo \_ RawCMCEvent**](msmcainfo-rawcmcevent.md)                             | Contient un événement CMC.                                                                                  |
| [**MSMCAInfo \_ RawCorrectedPlatformEvent**](msmcainfo-rawcorrectedplatformevent.md) | Contient un événement de plateforme corrigé.                                                                   |
| [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md)                               | Spécifie les journaux MCA bruts.                                                                            |
| [**MSMCAInfo \_ RawMCAEvent**](msmcainfo-rawmcaevent.md)                             | Contient un événement MCA.                                                                                  |
| [**WmiEvent**](wmievent.md)                                                        | Classe de base abstraite à partir de laquelle toutes les classes d’événements du fournisseur MCA sont dérivées.                             |



 

 

 



