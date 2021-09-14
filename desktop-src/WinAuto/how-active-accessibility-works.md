---
title: Fonctionnement de Active Accessibility
description: Microsoft Active Accessibility est conçu pour aider les aides à l’accessibilité, appelées clients, interagir avec les éléments d’interface utilisateur standard et personnalisés d’autres applications et du système d’exploitation.
ms.assetid: 29325f0a-c6ca-42b1-b85d-2671f7041034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdeffcebd96ffba804bfc24672bf867028e9b0c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191719"
---
# <a name="how-active-accessibility-works"></a>Fonctionnement de Active Accessibility

Microsoft Active Accessibility est conçu pour aider les aides à l’accessibilité, appelées *clients*, interagir avec les éléments d’interface utilisateur standard et personnalisés d’autres applications et du système d’exploitation. Un client Microsoft Active Accessibility est un programme qui utilise Microsoft Active Accessibility pour accéder, identifier ou manipuler les éléments d’interface utilisateur d’une application. Les clients incluent des aides à l’accessibilité, des outils de test automatisés et certaines applications de formation basées sur l’ordinateur.

À l’aide de Microsoft Active Accessibility, une application cliente peut :

-   Demander des informations ; par exemple, sur un élément d’interface utilisateur à un emplacement particulier.
-   Recevoir des notifications en cas de modification des informations ; par exemple, lorsqu’un contrôle est grisé ou lorsqu’une chaîne de texte change.
-   Effectuer des actions qui affectent l’interface utilisateur ou le contenu du document ; par exemple, cliquez sur un bouton de commande, déroulant un menu, puis choisissez une commande de menu.

Les applications qui interagissent avec et fournissent des informations pour les clients sont appelées *serveurs*. Un serveur utilise Microsoft Active Accessibility pour fournir des informations sur ses éléments d’interface utilisateur aux clients. Tout contrôle, module ou application qui utilise Microsoft Active Accessibility pour exposer des informations sur son interface utilisateur est considéré comme un serveur Microsoft Active Accessibility. Les serveurs communiquent avec les clients en envoyant des notifications d’événements (par exemple, en appelant [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)) et en répondant aux demandes des clients pour l’accès aux éléments de l’interface utilisateur (par exemple, la gestion des messages [**WM \_ GETOBJECT**](wm-getobject.md) envoyés depuis [*oleacc*](uiauto-glossary.md)). Les serveurs exposent des informations par le biais de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

À l’aide de Microsoft Active Accessibility, une application serveur peut :

-   Fournissez des informations sur ses objets d’interface utilisateur personnalisés et le contenu de ses fenêtres clientes.
-   Envoyer des notifications lorsque l’interface utilisateur change.

Par exemple, pour permettre à un utilisateur de sélectionner oralement des commandes à partir d’une barre d’outils personnalisée de traitement de texte, un programme de reconnaissance vocale doit avoir des informations sur cette barre d’outils. Le traitement de texte doit donc rendre ces informations disponibles. Microsoft Active Accessibility permet au traitement de texte d’exposer les informations relatives à sa barre d’outils personnalisée et au programme de reconnaissance vocale d’obtenir ces informations.

### <a name="client-applications-and-active-accessibility"></a>Applications clientes et Active Accessibility

Un client Microsoft Active Accessibility doit être averti lorsque l’interface utilisateur du serveur a été modifiée pour pouvoir communiquer ces informations à l’utilisateur. Pour vous assurer que le client est informé des modifications apportées à l’interface utilisateur, il utilise un mécanisme appelé événements de fenêtre, ou WinEvents, pour s’inscrire afin de recevoir des notifications. Pour plus d’informations, consultez [winEvents](winevents-infrastructure.md).

Pour en savoir plus sur et manipuler un élément d’interface utilisateur particulier, les clients utilisent l’interface COM (Component Object Model) de Microsoft Active Accessibility, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).

Un client peut récupérer un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour un élément d’interface utilisateur des quatre façons suivantes :

-   Appelez [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) et transmettez le handle de fenêtre de l’élément d’interface utilisateur.
-   Appelez [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) et transmettez un emplacement d’écran qui se trouve dans le rectangle englobant de l’élément d’interface utilisateur.
-   Définissez un hook WinEvent, recevez une notification et appelez [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) pour récupérer un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément d’interface utilisateur qui a généré l’événement.
-   Appelez une méthode [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) telle que [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) ou [**accédez à \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) pour accéder à un autre objet **IAccessible** .

 

 




