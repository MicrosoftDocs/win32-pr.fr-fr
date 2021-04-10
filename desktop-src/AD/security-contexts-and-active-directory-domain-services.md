---
title: Contextes de sécurité et Active Directory Domain Services
description: Quand une application est liée à un contrôleur de domaine Active Directory (DC), elle le fait dans le contexte de sécurité d’une entité de sécurité, qui peut être un utilisateur ou une entité, telle qu’un ordinateur ou un service système.
ms.assetid: 7ad0acbe-f81b-46d6-be87-3526b0bfbd1b
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, contextes de sécurité
- contextes de sécurité Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c337cb05f8158dbb90f231652c42fb10a486aef4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030982"
---
# <a name="security-contexts-and-active-directory-domain-services"></a>Contextes de sécurité et Active Directory Domain Services

Quand une application est liée à un contrôleur de domaine Active Directory (DC), elle le fait dans le contexte de sécurité d’une entité de sécurité, qui peut être un utilisateur ou une entité, telle qu’un ordinateur ou un service système. Le contexte de sécurité est le compte d’utilisateur utilisé par le système pour appliquer la sécurité lorsqu’un thread tente d’accéder à un objet sécurisable. Ces données incluent l’identificateur de sécurité (SID) de l’utilisateur, les appartenances aux groupes et les privilèges.

Un utilisateur établit un contexte de sécurité en présentant les informations d’identification pour l’authentification. Si les informations d’identification sont authentifiées, le système génère un jeton d’accès qui identifie les appartenances aux groupes et les privilèges associés au compte d’utilisateur. Le système vérifie votre jeton d’accès lorsque vous tentez d’accéder à un objet d’annuaire. Il compare les données de votre jeton d’accès aux comptes et groupes auxquels le descripteur de sécurité de l’objet a accordé ou refusé l’accès.

Utilisez les méthodes suivantes pour contrôler le contexte de sécurité avec lequel vous établissez une liaison à un contrôleur de Active Directory :

-   Liez à l’aide de l’option **\_ \_ d’authentification sécurisée ADS** avec la fonction [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) ou la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) et spécifiez explicitement un nom d’utilisateur et un mot de passe. Le système authentifie ces informations d’identification et génère un jeton d’accès qu’il utilise pour la vérification de l’accès pendant la durée de cette liaison. Pour en savoir plus, consultez [Authentification](authentication.md).
-   Établissez une liaison à l’aide de l’option **\_ \_ d’authentification sécurisée ADS** , mais sans spécifier d’informations d’identification. Si vous n’empruntez pas l’identité d’un utilisateur, le système utilise le contexte de sécurité principal de votre application, autrement dit, le contexte de sécurité de l’utilisateur qui a démarré votre application. Dans le cas d’un service système, il s’agit du contexte de sécurité du compte de service ou du compte LocalSystem.
-   Emprunter l’identité d’un utilisateur, puis établir une liaison avec **\_ \_ l’authentification sécurisée ADS**, mais sans spécifier d’informations d’identification. Dans ce cas, le système utilise le contexte de sécurité du client dont l’identité est empruntée. Pour plus d’informations, consultez [emprunt d’identité du client](/windows/desktop/SecAuthZ/client-impersonation).
-   Liez à l’aide de [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) avec l’option **\_ aucune \_ authentification ADS** . Cette méthode effectue une liaison sans authentification et génère « everyone » comme contexte de sécurité. Seul le fournisseur LDAP prend en charge cette option.

Si possible, liez sans spécifier d’informations d’identification. Autrement dit, utilisez le contexte de sécurité de l’utilisateur connecté ou du client dont l’identité est empruntée. Cela vous permet d’éviter la mise en cache des informations d’identification. Si vous devez utiliser d’autres informations d’identification de l’utilisateur, vous pouvez demander les informations d’identification, établir une liaison avec eux, mais pas les mettre en cache. Pour utiliser le même contexte de sécurité dans plusieurs opérations de liaison, vous pouvez spécifier le nom d’utilisateur et le mot de passe pour la première opération de liaison, puis spécifier uniquement le nom d’utilisateur pour effectuer des liaisons ultérieures. Pour plus d’informations sur l’utilisation de cette technique, consultez [authentification](authentication.md).

Certains contextes de sécurité sont plus puissants que d’autres. Par exemple, le compte LocalSystem sur un contrôleur de domaine dispose d’un accès complet à Active Directory Domain Services, alors qu’un utilisateur standard n’a qu’un accès limité à certains objets de l’annuaire. En général, votre application ne doit pas s’exécuter dans un contexte de sécurité puissant, tel que LocalSystem, lorsqu’un contexte de sécurité moins puissant suffit pour effectuer les opérations. Cela signifie que vous pouvez diviser votre application en composants distincts, chacun d’entre eux s’exécutant dans un contexte de sécurité adapté aux opérations à effectuer. Par exemple, la configuration de votre application peut être divisée comme suit :

-   Effectuez des modifications de schéma et des extensions dans le contexte d’un utilisateur qui est membre du groupe administrateurs de schéma.
-   Effectuez les modifications du conteneur de configuration dans le contexte d’un utilisateur membre du groupe administrateurs de l’entreprise.
-   Effectuez des modifications de conteneur de domaine dans le contexte d’un utilisateur membre du groupe administrateurs de domaine.

 

 