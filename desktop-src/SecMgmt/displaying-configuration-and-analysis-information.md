---
description: Votre extension de composant logiciel enfichable doit afficher les informations de configuration et d’analyse actuelles pour les utilisateurs.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Affichage des informations de configuration et d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009021"
---
# <a name="displaying-configuration-and-analysis-information"></a>Affichage des informations de configuration et d’analyse

Votre extension de composant logiciel enfichable doit afficher les informations de configuration et d’analyse actuelles pour les utilisateurs.

Pour afficher les informations, le nœud extension du composant logiciel enfichable d’attachement doit étendre les composants logiciels enfichables de configuration de sécurité à l’aide du nœud services. Le nœud services est le composant logiciel enfichable MMC qui administre les services installés sur le système.

Les types de nœuds pouvant être étendus sont les suivants :

-   Services de configuration NodeType = {24a7f717-1f0c-11D1-AFFB-00C04FB984F9}
-   Services d’inspection NodeType = {678050c7-1ff8-11D1-AFFB-00C04FB984F9}

Lorsque le nœud services est développé, la console MMC avertit toutes les extensions de composant logiciel enfichable inscrites. Chaque composant logiciel enfichable d’une pièce jointe doit s’insérer dans le nœud services et effectuer les tâches suivantes :

-   Appelez **QueryInterface** pour obtenir un pointeur vers l’interface [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) exposée par les composants logiciels enfichables de configuration de la sécurité.
-   Appelez [**ISceSvcAttachmentData :: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) pour informer les composants logiciels enfichables de configuration de sécurité que l’extension du composant logiciel enfichable est chargée et pour établir un contexte de communication.
-   Appelez [**ISceSvcAttachmentData :: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) pour récupérer les informations de configuration de la base de données. Cette étape peut être effectuée lorsque l’extension du composant logiciel enfichable s’initialise lui-même ou lorsque l’utilisateur ouvre son nœud.

Pour plus d’informations, consultez [Ajout d’un nœud extension de composant logiciel enfichable d’une pièce jointe](adding-an-attachment-snap-in-extension-node.md).

 

 



