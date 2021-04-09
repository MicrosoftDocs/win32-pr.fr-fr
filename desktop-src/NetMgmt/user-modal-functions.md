---
title: Fonctions modales utilisateur
description: Les fonctions modales utilisateur de gestion de réseau obtiennent et définissent des paramètres à l’ensemble du système liés au comportement du système de sécurité.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941298"
---
# <a name="user-modal-functions"></a>Fonctions modales utilisateur

Les fonctions modales utilisateur de gestion de réseau obtiennent et définissent des paramètres à l’ensemble du système liés au comportement du système de sécurité.

Les fonctions modales utilisateur sont répertoriées ci-dessous.



| Fonction                                     | Description                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Retourne des informations globales pour tous les utilisateurs et groupes globaux dans la base de données de sécurité, qui est la base de données du gestionnaire de comptes de sécurité (SAM) ou, dans le cas des contrôleurs de domaine, la Active Directory. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Définit des informations globales pour tous les utilisateurs et groupes globaux dans la base de données de sécurité.                                                                                                                       |



 

Les fonctions **NetUserModalsGet** et **NetUserModalsSet** examinent et modifient les paramètres modaux, qui sont des paramètres globaux qui affectent chaque compte de la base de données de sécurité (par exemple, la longueur minimale autorisée pour le mot de passe). Tous les paramètres modaux peuvent être modifiés en appelant **NetUserModalsSet**. La plupart des modaux peuvent également être modifiés à l’aide de la commande **net Accounts** . Les fonctions modales de l’utilisateur de gestion de réseau ne nécessitent pas que le serveur dispose d’une sécurité au niveau de l’utilisateur.

Les informations modales de l’utilisateur sont disponibles aux niveaux suivants :

-   [**\_Informations sur les modales utilisateur \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [**\_Informations sur les modaux utilisateur \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [**\_Informations sur les modales utilisateur \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [**Informations sur les modaux de l’utilisateur \_ \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

Les niveaux d’informations suivants sont valides uniquement pour [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) et remplacent l’ancien moyen de passer un *Parmnum* pour définir un champ spécifique :

-   [**\_Informations sur les modaux utilisateur \_ \_ 1001**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [**\_Informations sur les modaux utilisateur \_ \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [**\_Informations sur les modaux utilisateur \_ \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [**\_Informations sur les modaux utilisateur \_ \_ 1004**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [**\_Informations sur les modaux utilisateur \_ \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [**\_Informations sur les modaux utilisateur \_ \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [**\_Informations sur les modaux utilisateur \_ \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions modales utilisateur de gestion de réseau. Pour plus d’informations, consultez [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).

 

 