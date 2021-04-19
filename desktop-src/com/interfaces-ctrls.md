---
title: Interfaces (contrôles et pages de propriétés)
description: Les interfaces suivantes sont utilisées pour créer des objets COM standard et des pages de propriétés.
ms.assetid: f0d655b3-fa92-4553-ba21-617649a922a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e143ab1793eaf0335bbcf04093707bdc359e868e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106513758"
---
# <a name="interfaces-controls-and-property-pages"></a>Interfaces (contrôles et pages de propriétés)

Les interfaces suivantes sont utilisées pour créer des objets COM standard et des pages de propriétés.



| Interface                                             | Description                                                                                                                                                                                                  |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)                                | Fournit un wrapper autour d’un objet de police Windows.                                                                                                                                                             |
| [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)                        | Expose les propriétés d’un objet font par le biais de l’automatisation. Il fournit un sous-ensemble des méthodes [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .                                                                                           |
| [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol)                    | Fournit les fonctionnalités pour la prise en charge des mnémoniques du clavier, des propriétés ambiantes et des événements dans les objets de contrôle.                                                                                                  |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)            | Fournit les méthodes qui permettent à un objet de site de gérer chaque contrôle incorporé dans un conteneur.                                                                                                           |
| [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)  | Récupère les informations dans les pages de propriétés fournies par un objet.                                                                                                                                        |
| [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture)                          | Gère un objet image et ses propriétés. Les objets image fournissent une abstraction indépendante du langage pour les bitmaps, les icônes et les fichiers.                                                                       |
| [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)                  | Expose les propriétés de l’objet Picture par le biais de l’automatisation. Il fournit un sous-ensemble des fonctionnalités disponibles par le biais des méthodes [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .                                                |
| [**IPointerInactive**](/windows/desktop/api/OCIdl/nn-ocidl-ipointerinactive)          | Permet à un objet de rester inactif la plupart du temps, tout en participant à l’interaction avec la souris, y compris le glisser-déplacer.                                                                         |
| [**IPrint**](/windows/desktop/api/DocObj/nn-docobj-iprint)                              | Active les documents composés en général et les documents actifs, en particulier pour prendre en charge l’impression par programmation.                                                                                                   |
| [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)    | Implémenté par un objet récepteur pour recevoir des notifications sur les modifications de propriété d’un objet qui prend en charge [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) comme interface sortante.                       |
| [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)                | Fournit les principales fonctionnalités d’un objet page de propriétés qui gère une page particulière dans une feuille de propriétés.                                                                                                 |
| [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)              | Extension de [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) pour prendre en charge la sélection initiale d’une propriété sur une page.                                                                                                 |
| [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite)        | Fournit les principales fonctionnalités d’un objet de site de page de propriétés.                                                                                                                                                  |
| [**IQuickActivate**](/windows/desktop/api/OCIdl/nn-ocidl-iquickactivate)              | Permet aux contrôles et aux conteneurs d’éviter les goulots d’étranglement de performances lors du chargement des contrôles. Il combine la négociation au moment du chargement ou de l’initialisation entre le contrôle et son conteneur dans un appel unique. |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)          | Fournit des contrôles Frame simples qui jouent le rôle de conteneurs simples pour d’autres contrôles imbriqués.                                                                                                                      |
| [**ISpecifyPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages) | Indique qu’un objet prend en charge les pages de propriétés.                                                                                                                                                            |



 

 

 
