---
description: L’objectif du wrapper de fournisseur est d’encapsuler et d’utiliser les interfaces COM de bas niveau (fournies par les fabricants de cartes à puce) pour une carte à puce particulière. Ces interfaces ne sont pas fournies par Microsoft.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Fournisseur de services de wrappers de fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096201"
---
# <a name="vendor-wrapper-service-provider"></a>Fournisseur de services de wrappers de fournisseur

L’objectif du wrapper de fournisseur est d’encapsuler et d’utiliser les interfaces COM de bas niveau (fournies par les fabricants de cartes à puce) pour une carte à puce particulière. Ces interfaces ne sont pas fournies par Microsoft.

![Wrapper de fournisseur](images/scspart1.png)

Comme décrit dans la partie 6 de la *spécification d’interopérabilité pour les ICCS et les systèmes d’ordinateurs personnels* (consultez les spécifications à [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) l’adresse), la fonctionnalité exposée par ce wrapper est plus facile à utiliser que les fonctionnalités de quatre fournisseurs de services distincts. La fonctionnalité du wrapper peut être divisée en quatre zones principales :

-   Services d’authentification par carte à puce, tels que l’authentification par stimulation et l’authentification par carte.
-   Accès aux fichiers de carte à puce ou services de système de fichiers, tels que ouvrir, fermer, lire et écrire.
-   Gestion des cartes à puce, telle que l’attachement et le détachement.
-   Services de vérification de carte à puce, tels que vérifier et modifier le code.

> [!Note]  
> Cette spécification peut ne pas être disponible dans certains langages, pays ou régions.

 

La fonctionnalité est spécifique au type de carte utilisé (fonction prise en charge par la carte, protocoles, etc.) et sera différente pour chaque carte.

L’exemple de wrapper Microsoft SCardCOM utilise la bibliothèque COM ATL pour implémenter un wrapper simple et définir un modèle pour d’autres wrappers. Il implémente les interfaces suivantes.



| Interface ou objet                                     | Description                         |
|---------------------------------------------------------|-------------------------------------|
| [**ISCardAuth**](iscardauth.md)<br/>             | Services d’authentification.<br/> |
| [**ISCardFileAccess**](iscardfileaccess.md)<br/> | Services du système de fichiers.<br/>    |
| [**ISCardManage**](iscardmanage.md)<br/>         | Services de gestion.<br/>     |
| [**ISCardVerify**](iscardverify.md)<br/>         | Services de vérification.<br/>   |



 

> [!Note]  
> L’exemple SCardCOM est fourni uniquement comme exemple d’implémentation des interfaces de wrapper. Pour éviter les conflits de noms de DLL avec d’autres fournisseurs, vous ne devez pas utiliser SCardCOM.dll comme nom des dll que vous créez.

 

Voici une utilisation courante du wrapper du fournisseur. Cet exemple utilise l’interface [**ISCardManage**](iscardmanage.md) pour créer des instances des interfaces qui seront encapsulées dans le fournisseur de services et l’interface [**ISCardVerify**](iscardverify.md) pour vérifier leur opération.

**Pour générer un fournisseur de services de wrapper**

1.  Créez une instance de l’interface [**ISCardManage**](iscardmanage.md) . Utilisez cette interface pour créer une instance des interfaces requises (par exemple, [**ISCardFileAccess**](iscardfileaccess.md) ou [**ISCardVerify**](iscardverify.md)). Lors de la création de ces interfaces, les interfaces COM de bas niveau correspondantes sont également créées.
2.  Connectez/Connectez-vous à une carte par le biais de la méthode [**ISCardManage**](iscardmanage.md) appropriée.
3.  Effectuez les opérations requises par le biais de la méthode [**ISCardVerify**](iscardverify.md) appropriée (qui peut appeler plusieurs méthodes et interfaces COM de bas niveau pour se terminer).
4.  Répétez cette opération pour les autres opérations.
5.  Mise en version terminée.

Le nom de l’interface COM et l’identificateur d’interface (GUID) ne doivent pas changer par rapport à ceux utilisés dans le wrapper de code ou d’exemple. Toutefois, le GUID de la classe (autrement dit, où une implémentation réelle de l’interface réside) doit être modifié par rapport à ceux utilisés. Cela est particulièrement important lors de l’implémentation d’un wrapper de fournisseur. Un exemple consiste à utiliser plusieurs wrappers de fournisseur sur un ordinateur particulier. Ces wrappers doivent implémenter les mêmes interfaces COM, mais utilisent toujours des stratégies d’implémentation différentes. Par conséquent, des classes différentes (et des ID de classe) sont requises.

 

 




