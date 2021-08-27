---
title: à propos de l’API Windows Deployment Services
description: Windows les Services de déploiement (WDS) sont une suite de composants qui permettent de déployer des systèmes d’exploitation Windows, en particulier Windows Vista et versions ultérieures, ainsi que Windows Server 2008 et versions ultérieures.
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Windows services de déploiement Windows les services de déploiement, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd65f18c1628236358d61656c8c3b414d180e43166daa86dfa6562024252a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098679"
---
# <a name="about-the-windows-deployment-services-api"></a>à propos de l’API Windows Deployment Services

Windows les Services de déploiement (WDS) sont une suite de composants qui permettent de déployer des systèmes d’exploitation Windows, en particulier Windows Vista et versions ultérieures, ainsi que Windows Server 2008 et versions ultérieures. Vous pouvez l’utiliser pour configurer de nouveaux ordinateurs à l’aide d’installations réseau.

les fabricants d’ordinateurs oem, les intégrateurs de systèmes et les professionnels de l’informatique qui recherchent des informations sur la façon de déployer des Windows sur de nouveaux ordinateurs doivent voir les informations sur la solution WDS standard dans le [Guide pas à pas de la mise à jour des Services de déploiement Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) et le [Kit d’installation automatisée (Windows AIK) (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

Dans les environnements où la solution WDS standard ne peut pas être utilisée, l’API WDS autorise l’accès par programmation à certains composants de WDS.

-   les [fonctions de serveur Windows Deployment Services](windows-deployment-services-server-functions.md) fournissent un accès par programme au serveur WDS environnement PXE (Preboot Execution Environment) (PXE). Les composants serveur WDS incluent un serveur PXE et un serveur TFTP (trivial protocole FTP) pour le démarrage réseau d’un ordinateur afin de charger et d’installer un système d’exploitation.
-   les [fonctions du client Windows Deployment Services](windows-deployment-services-client-functions.md) fournissent un accès par programme au client WDS. les composants du client WDS incluent une interface utilisateur graphique qui s’exécute dans l’environnement de préinstallation Windows (Windows PE) et communique avec les composants serveur pour sélectionner et installer une image du système d’exploitation.
-   Il n’existe aucune API pour les composants de gestion WDS. Ces composants sont un ensemble d’outils que vous utilisez pour gérer le serveur, les images du système d’exploitation et les comptes d’ordinateur client. pour plus d’informations sur les composants de gestion WDS, consultez [le Guide pas à pas de la mise à jour des Services de déploiement Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).

Le serveur PXE WDS se compose d’un serveur PXE et d’un fournisseur PXE. Le serveur PXE contient la fonctionnalité de mise en réseau de base. Le serveur PXE prend en charge les interfaces de plug-in qui sont appelées fournisseurs PXE. Ce modèle de fournisseur permet le développement de solutions PXE personnalisées tout en continuant à utiliser la base de code réseau principale du serveur PXE.

-   les développeurs peuvent utiliser les [fonctions de serveur Windows Deployment Services](windows-deployment-services-server-functions.md) pour écrire une DLL pour un fournisseur personnalisé à remplacer ou exécuter conjointement avec la couche de négociation d’informations de démarrage (BINL) standard sur un serveur WDS. Par exemple, le fournisseur personnalisé peut utiliser un fichier texte comme magasin de données au lieu de Active Directory.
-   les développeurs peuvent utiliser les [fonctions de serveur Windows Deployment Services](windows-deployment-services-server-functions.md) pour écrire un fournisseur de filtres qui est séquencé avant BINL, ou tout autre fournisseur PXE, dans la liste triée des fournisseurs inscrits. Le deuxième fournisseur traite ensuite uniquement les demandes PXE sélectionnées, tandis que le premier fournisseur gère d’autres requêtes. Par exemple, cela peut permettre au deuxième fournisseur inscrit dans la liste triée d’offrir de nouvelles fonctionnalités sans interrompre la solution WDS existante implémentée dans le premier fournisseur.

le client WDS comprend une interface utilisateur graphique qui s’exécute dans l’environnement de préinstallation Windows (Windows PE) et communique avec les composants serveur pour sélectionner et installer une image du système d’exploitation. La bibliothèque cliente WDS prend en charge le développement d’applications clientes personnalisées qui peuvent utiliser un serveur WDS.

-   les développeurs peuvent utiliser les [fonctions du client Windows Deployment Services](windows-deployment-services-client-functions.md) pour écrire leur propre application cliente personnalisée qui remplace le client WDS. Par exemple, l’application personnalisée peut énumérer les images stockées sur un serveur WDS et envoyer des messages de progression de l’installation au journal des événements du serveur PXE.

## <a name="windows-deployment-services-samples"></a>Windows Exemples de services de déploiement

un exemple de fournisseur PXE personnalisé, de fournisseur de filtres et d’application cliente WDS est disponible dans le kit de développement logiciel (sdk) de microsoft Windows, consultez le [kit de développement logiciel (sdk) de microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/).

Vous pouvez télécharger les exemples WDS suivants en ligne dans la [Galerie de code du Bureau](https://github.com/microsoft/Windows-classic-samples).

<dl>

[Windows Exemple de fournisseur de filtres des services de déploiement](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Exemple d’énumération d’images des services de déploiement](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Windows Exemple de consommateur de multidiffusion des services de déploiement](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Exemple de fournisseur de multidiffusion des services de déploiement](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Exemple de fournisseur de services de déploiement](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Exemple de gestionnaire de transport des services de déploiement](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’API du serveur des Services de déploiement Windows](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[Utilisation de l’API du client des Services de déploiement Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 