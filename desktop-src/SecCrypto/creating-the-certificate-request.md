---
description: Le processus de création d’une demande de certificat implique la collecte de certaines informations auprès du demandeur.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Création de la demande de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228959"
---
# <a name="creating-the-certificate-request"></a>Création de la demande de certificat

Le processus de création d’une demande de certificat implique la collecte de certaines informations auprès du demandeur. En général, cette opération s’effectue par le biais d’une interface utilisateur, bien que les informations puissent être extraites directement d’une base de données sans avoir besoin d’une interface utilisateur. Le niveau d’information requis est défini par la stratégie de l' [*autorité de certification*](../secgloss/c-gly.md) .

Voici un exemple des informations requises :

-   Nom commun
-   Nom de l’unité
-   Nom de l’entreprise
-   City
-   State
-   Pays/Région

> [!Note]  
> L’interface est conçue pour effectuer une seule requête pour chaque instance de xenroll. Une instance xenroll distincte doit être créée pour créer chaque [*demande de certificat*](../secgloss/c-gly.md).

 

Pour plus d’informations sur l’utilisation du contrôle d’inscription de certificats pour demander un certificat dans des langages de programmation spécifiques, consultez les rubriques suivantes :

-   [Exemple de demande en C++](request-sample-in-c-.md)
-   [Exemple de demande dans VBScript](request-sample-in-vbscript.md)

 

 
