---
description: WMI s’appuie sur les descripteurs de sécurité Windows standard pour contrôler et protéger l’accès aux objets sécurisables tels que les espaces de noms WMI, les imprimantes, les services et les applications DCOM.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Accès aux objets sécurisables WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210220"
---
# <a name="access-to-wmi-securable-objects"></a>Accès aux objets sécurisables WMI

WMI s’appuie sur les [*descripteurs de sécurité*](/windows/desktop/SecGloss/s-gly) Windows standard pour contrôler et protéger l’accès aux objets sécurisables tels que les espaces de noms WMI, les imprimantes, les services et les applications DCOM. Pour plus d’informations, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md).

Les rubriques suivantes sont présentées dans cette section :

-   [Descripteurs de sécurité et sid](#security-descriptors-and-sids)
-   [Contrôle d’accès](#access-control)
-   [Modification de la sécurité d’accès](#changing-access-security)
-   [Rubriques connexes](#related-topics)

## <a name="security-descriptors-and-sids"></a>Descripteurs de sécurité et sid

WMI maintient la sécurité d’accès en comparant le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) de l’utilisateur qui tente d’accéder à un objet sécurisable avec le descripteur de sécurité de l’objet.

Lorsqu’un utilisateur ou un groupe est créé sur un système, le SID s’assure [*qu’un compte*](/windows/desktop/SecGloss/s-gly) créé avec le même nom qu’un compte supprimé précédemment n’hérite pas des paramètres de sécurité précédents. Un jeton d’accès est créé en combinant le SID, la liste des groupes dont l’utilisateur est membre et la liste des privilèges activés ou désactivés. Ces jetons sont affectés à tous les processus et threads appartenant à l’utilisateur.

## <a name="access-control"></a>Contrôle d’accès

Lorsque l’utilisateur souhaite utiliser un objet sécurisé, le jeton d’accès est comparé à la [*liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) dans le descripteur de sécurité de l’objet. La liste DACL contient des autorisations appelées [*entrées de contrôle d’accès (ACE)*](/windows/desktop/SecGloss/a-gly). Les [*listes de contrôle d’accès système (SACL)*](/windows/desktop/SecGloss/s-gly) font la même chose que les DACL, mais elles peuvent générer des événements d’audit de sécurité. À compter de Windows Vista, WMI peut créer des entrées d’audit dans le journal de sécurité Windows. Pour plus d’informations sur l’audit dans WMI, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md).

Les listes DACL et SACL se composent toutes deux d’une liste d’entrées de contrôle d’accès qui décrivent les utilisateurs ayant des droits d’accès spécifiques, y compris l’écriture dans le référentiel WMI, l’accès et l’exécution à distance et les autorisations d’ouverture de session. WMI stocke ces listes de contrôle d’accès dans l’espace de stockage WMI.

Les ACE contiennent trois types de niveaux d’accès ou des droits accord/refus : autoriser, refuser pour DACL et audit système (pour les listes SACL). Les ACE de refus précèdent les ACE Allow dans la liste DACL ou SACL. Lors de la vérification des droits d’accès utilisateur, WMI s’exécute de manière consécutive via la liste de contrôle d’accès jusqu’à ce qu’il trouve un ACE Allow qui s’applique au jeton d’accès demandeur. Les ACE restantes ne sont pas vérifiées après ce point. Si aucun ACE allow approprié n’est trouvé, l’accès est refusé. Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) et [création d’une liste DACL](/windows/desktop/SecBP/creating-a-dacl).

## <a name="changing-access-security"></a>Modification de la sécurité d’accès

Avec les autorisations appropriées, vous pouvez modifier la sécurité sur un objet sécurisable à l’aide d’un script ou d’une application. Vous pouvez également modifier les paramètres de sécurité sur les espaces de noms WMI à l’aide du [*contrôle WMI*](gloss-w.md) ou en ajoutant une chaîne [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) dans le fichier [*format MOF (MOF)*](gloss-m.md) qui définit les classes de l’espace de noms. Pour plus d’informations, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md), [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)et [modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets descripteurs de sécurité WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> <dt>

[Contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md)
</dt> <dt>

[Objets descripteurs de sécurité WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
