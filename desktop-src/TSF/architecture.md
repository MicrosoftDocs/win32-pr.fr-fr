---
title: Architecture (Text Services Framework)
description: Architecture
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Text Services Framework (TSF), architecture
- TSF (Text Services Framework), architecture
- services de texte, architecture
- Applications compatibles TSF, architecture
- Text Services Framework (TSF), composants
- TSF (Text Services Framework), composants
- services de texte, composants
- Applications compatibles TSF, composants
- Text Services Framework (TSF), applications
- TSF (Text Services Framework), applications
- services de texte, applications
- Applications compatibles TSF, à propos de
- Text Services Framework (TSF), text services
- TSF (Text Services Framework), services de texte
- services de texte, à propos de
- Applications compatibles TSF, services de texte
- Text Services Framework (TSF), gestionnaire TSF
- TSF (Text Services Framework), gestionnaire TSF
- services de texte, gestionnaire TSF
- Applications compatibles TSF, gestionnaire TSF
- Gestionnaire TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193576"
---
# <a name="architecture-text-services-framework"></a>Architecture (Text Services Framework)

Text Services Framework comprend trois composants principaux :

-   **Applications :** Les opérations d’application incluent généralement l’affichage, la modification directe et le stockage de texte. Une application fournit l’accès au texte en implémentant un serveur COM qui prend en charge certaines interfaces et communique avec TSF à l’aide des interfaces exposées par le gestionnaire TSF. Tout au long de cette documentation, le terme, application, fait référence à une application compatible TSF, sauf indication contraire.
-   **Services de texte :** Un service de texte fonctionne comme un fournisseur de texte pour une application. Un service de texte peut obtenir du texte à partir d’une application, et écrire du texte dans celle-ci. Un service de texte peut également associer des données et des propriétés à un bloc de texte. Un service de texte est implémenté en tant que serveur COM in-proc qui s’inscrit auprès de TSF. Une fois inscrit, l’utilisateur interagit avec le service de texte à l’aide de la barre de langue ou des raccourcis clavier. Plusieurs services de texte peuvent être installés.
-   **Gestionnaire TSF :** Le gestionnaire TSF fonctionne comme médiateur entre une application et un ou plusieurs services de texte. Un service de texte n’interagit jamais directement avec une application. Toutes les communications passent par le gestionnaire TSF. Le gestionnaire TSF est implémenté par le système d’exploitation et ne peut pas être remplacé. Dans cette documentation, le terme, Manager, fait référence au gestionnaire TSF, sauf indication contraire.

L’illustration suivante montre les principaux éléments architecturaux de TSF.

![architecture de l’infrastructure de services de texte](images/tsf-arch.gif)

Avec cette architecture, le gestionnaire TSF fournit une couche d’abstraction entre les applications et les services de texte. Cette couche d’abstraction permet à une application et à un ou plusieurs services de texte de partager du texte, et elle permet au gestionnaire TSF de gérer les services de texte.

 

 




