---
description: .
ms.assetid: 72a77e83-ab18-438c-af11-fa6d55bf0180
title: Administrateur de compatibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abde760ca7324aec18f0576a7f04e3a4c5db2d22
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314982"
---
# <a name="compatibility-administrator"></a>Administrateur de compatibilité

## <a name="affected-platforms"></a>Plateformes affectées

 **Clients :** Windows 2000, Windows XP, Windows Vista, Windows 7  
**Serveurs :** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="description"></a>Description

L’outil d’administration de la compatibilité, fourni par application Compatibility Toolkit (ACT), vous permet de résoudre un grand nombre de problèmes potentiels de compatibilité des applications, avant de déployer une nouvelle version de Windows dans votre organisation, en procédant comme suit :

-   Fournir des correctifs de compatibilité individuels, des modes de compatibilité et des messages AppHelp que vous pouvez utiliser pour résoudre des problèmes de compatibilité spécifiques
-   Vous permet de créer des correctifs de compatibilité personnalisés, des modes de compatibilité, des messages AppHelp et des bases de données de compatibilité
-   Fournir un outil de requête qui vous permet de rechercher les correctifs installés sur vos ordinateurs locaux

## <a name="usage"></a>Utilisation

L’organigramme suivant illustre les étapes nécessaires à l’utilisation de l’administrateur de compatibilité pour créer vos correctifs de compatibilité, modes de compatibilité et messages AppHelp.



|                                            |          |                                                                                            |          |                                                     |          |                                                                             |
|--------------------------------------------|----------|--------------------------------------------------------------------------------------------|----------|-----------------------------------------------------|----------|-----------------------------------------------------------------------------|
| Créer une nouvelle base de données de compatibilité (. sdb) | **>** | Sélectionnez l’application, puis sélectionnez les correctifs de compatibilité à appliquer à l’application. | **>** | Tester l’application avec le nouveau correctif de compatibilité | **>** | Enregistrez la base de données de compatibilité, puis déployez le correctif dans votre entreprise |



 

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Téléchargement de l’outil Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)
-   [Utilisation de l’administrateur de compatibilité](/previous-versions/windows/it-pro/windows-7/cc749034(v=ws.10))
-   [Correctifs de compatibilité connus, modes de compatibilité et messages AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [Test et atténuation des problèmes à l’aide des outils de développement](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))

 

 
