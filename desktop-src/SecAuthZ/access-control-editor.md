---
description: Ensemble de feuilles de propriétés et de pages de propriétés qui permettent à l’utilisateur d’afficher et de modifier les composants d’un descripteur de sécurité d’objets.
ms.assetid: ca709f27-8463-4f11-92ac-2148796e640a
title: Éditeur de Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65117fe086b6a374dbd973f2cb657ec9c19cc3a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013763"
---
# <a name="access-control-editor"></a>Éditeur de Access Control

L’éditeur de contrôle d’accès est un ensemble de feuilles de propriétés et de pages de propriétés qui permettent à l’utilisateur d’afficher et de modifier les composants du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)d’un objet. L’éditeur se compose de deux parties principales :

-   Une [page de propriétés de sécurité de base](basic-security-property-page.md) qui fournit une interface simple pour la modification des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) dans la liste de [*contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) d’un objet. Cette page peut inclure un bouton **avancé** facultatif qui affiche la feuille de propriétés de sécurité avancée.
-   [Feuille de propriétés de sécurité avancée](advanced-security-property-sheet.md) avec des pages de propriétés qui permettent à l’utilisateur de modifier la [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) de l’objet, de modifier le propriétaire de l’objet ou d’effectuer une modification avancée de la liste DACL de l’objet.

La fonction [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) crée la page de propriétés de sécurité de base. Vous pouvez ensuite utiliser la fonction [**feuille**](/windows/win32/api/prsht/nf-prsht-propertysheeta) ou le message de la [**\_ ADDPAGE PSM**](../controls/psm-addpage.md) pour ajouter cette page à une feuille de propriétés.

Vous pouvez également utiliser la fonction [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) pour afficher une feuille de propriétés qui contient la page de propriétés de sécurité de base.

Pour [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) et [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity), l’appelant doit passer un pointeur vers une implémentation de l’interface [**ISecurityInformation**](/windows/win32/api/aclui/nn-aclui-isecurityinformation) . L’éditeur de contrôle d’accès appelle les méthodes de cette interface pour récupérer des informations de contrôle d’accès sur l’objet en cours de modification et pour repasser l’entrée de l’utilisateur à votre application. Les méthodes **ISecurityInformation** ont les objectifs suivants :

-   Pour initialiser les pages de propriétés.

    Votre implémentation de la méthode [**GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) passe une structure d' [**\_ \_ informations d’objet si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) à l’éditeur. Cette structure spécifie les pages de propriétés que l’éditeur doit afficher, ainsi que d’autres informations qui déterminent les options de modification disponibles pour l’utilisateur.

-   Pour fournir des informations de sécurité sur l’objet en cours de modification.

    Votre implémentation de [**GetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getsecurity) passe le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) initial de l’objet à l’éditeur. Les méthodes [**GetAccessRights**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getaccessrights) et [**MapGeneric**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-mapgeneric) fournissent des informations sur les droits d’accès de l’objet. La méthode [**GetInheritTypes**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getinherittypes) fournit des informations sur la façon dont les objets enfants peuvent hériter des ACE de l’objet.

-   Pour renvoyer l’entrée de l’utilisateur à votre application.

    Quand l’utilisateur clique sur **OK** ou sur **appliquer**, l’éditeur appelle votre méthode [**SetSecurity**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-setsecurity) pour renvoyer un descripteur de sécurité contenant les modifications de l’utilisateur.

 

 
