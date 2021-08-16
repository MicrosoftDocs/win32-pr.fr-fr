---
title: Fonctionnement de Access Control dans Active Directory Domain Services
description: le contrôle d’accès pour les objets dans Active Directory Domain Services est basé sur les modèles de contrôle d’accès Windows NT et Windows 2000.
ms.assetid: 70eed84b-ada0-48e7-b448-704586e9afaa
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, sécurité, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f53cdd7b958313b3cb16bc538addc73b42bd0dc917160176422b85c959c8c05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188285"
---
# <a name="how-access-control-works-in-active-directory-domain-services"></a>Fonctionnement de Access Control dans Active Directory Domain Services

le contrôle d’accès pour les objets dans Active Directory Domain Services est basé sur les modèles de contrôle d’accès Windows NT et Windows 2000. Pour plus d’informations et pour obtenir une description détaillée de ce modèle et de ses composants, tels que les descripteurs de sécurité, les jetons d’accès, les SID, les ACL et les ACE, consultez [Access Control modèle](/windows/desktop/SecAuthZ/access-control-model).

Les privilèges d’accès pour les ressources de Active Directory Domain Services sont généralement accordées via l’utilisation d’une entrée de contrôle d’accès (ACE). Une entrée du contrôle d’accès définit une autorisation d’accès ou d’audit sur un objet pour un utilisateur ou un groupe spécifique. Une liste de contrôle d’accès (ACL) est la collection ordonnée d’entrées de contrôle d’accès définie pour un objet. Un descripteur de sécurité prend en charge les propriétés et les méthodes qui créent et gèrent des ACL. pour plus d’informations sur les modèles de sécurité, consultez [sécurité](/windows/desktop/SecAuthZ/access-control) ou le *Kit de ressources du serveur Windows 2000*. (Cette ressource n’est peut-être pas disponible dans certaines langues et pays ou régions.)

Le plan de base du modèle de sécurité est le suivant :

-   Descripteur de sécurité. Chaque objet d’annuaire possède son propre descripteur de sécurité qui contient des données de sécurité qui protègent l’objet. Le descripteur de sécurité peut contenir une liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List). Une liste DACL contient une liste d’ACE. Chaque ACE accorde ou refuse un ensemble de droits d’accès à un utilisateur ou à un groupe. Les droits d’accès correspondent aux opérations, telles que la lecture et l’écriture de propriétés, qui peuvent être effectuées sur l’objet.
-   Contexte de sécurité. Lors de l’accès à un objet d’annuaire, l’application spécifie les informations d’identification du principal de sécurité qui effectue la tentative d’accès. Une fois authentifiés, ces informations d’identification déterminent le contexte de sécurité de l’application, qui comprend les appartenances aux groupes et les privilèges associés au principal de sécurité. Pour plus d’informations sur les contextes de sécurité, consultez [contextes de sécurité et Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).
-   Vérification de l’accès. Le système accorde l’accès à un objet uniquement si le descripteur de sécurité de l’objet accorde les droits d’accès nécessaires au principal de sécurité qui tente l’opération (ou aux groupes auxquels le principal de sécurité appartient).

Le tableau suivant répertorie les interfaces ADSI utilisées pour manipuler les fonctionnalités de contrôle d’accès de Active Directory Domain Services.



| Interface                                                 | Description                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------|
| [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) | Utilisé pour lire et écrire les propriétés de sécurité d’un objet de service d’annuaire. |
| [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)   | Utilisé pour gérer et énumérer tous les ACE pour un objet de service d’annuaire.     |
| [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) | Utilisé pour lire et écrire des propriétés d’entrée du contrôle d’accès.                                    |



 

 

 