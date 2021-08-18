---
title: Conditions préalables à l’installation d’une extension de schéma
description: Pour modifier le schéma, assurez-vous de disposer des droits suivants et tenez compte des informations suivantes. vous devez disposer des droits suffisants pour modifier le schéma.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af50626d452c8e26cbf1e7d33addfcea4f854cd2b40b0860bb98c783044748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185301"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a>Conditions préalables à l’installation d’une extension de schéma

Pour modifier le schéma, assurez-vous de disposer des droits suivants et tenez compte des informations suivantes :

-   Vous devez disposer des droits suffisants pour modifier le schéma. Le schéma contient toutes les définitions de données pour Active Directory Domain Services pour l’ensemble de l’entreprise. Pour mettre à jour le schéma, un utilisateur doit être membre du groupe administrateurs du schéma, ou les droits de mise à jour du schéma ont été délégués.
-   Vous ne pouvez apporter des modifications de schéma qu’au contrôleur de schéma. Pour plus d’informations, consultez [détection du contrôleur de schéma](detecting-the-schema-master.md).
-   Le contrôleur de schéma doit être accessible en écriture ; autrement dit, le verrouillage de sécurité dans le registre doit être supprimé. Pour plus d’informations, consultez [la page activation des modifications de schéma sur le contrôleur de schéma](enabling-schema-changes-at-the-schema-master.md).
-   Pour plus d’informations sur la façon de vérifier si le contrôleur de schéma peut être modifié et sur la façon de modifier ses paramètres, consultez « XADM : impossible de mettre à jour le schéma sur le propriétaire du schéma » dans la base de connaissances d’aide et de support à l’adresse [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .

 

 




