---
title: Informations sur la version
description: Cette section traite de la ressource d’informations sur la version.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\versioninformation.htm
keywords:
- ressources, informations sur la version
- informations de version
- numéros de version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e43de27f18f89a5f240242b63ade057f57ec92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310105"
---
# <a name="version-information"></a>Informations sur la version

Les informations de version facilitent l’installation correcte des fichiers par les applications et permet aux programmes d’installation d’analyser les fichiers actuellement installés. La ressource informations sur la version contient le numéro de version du fichier, le système d’exploitation prévu et le nom de fichier d’origine.

### <a name="in-this-section"></a>Dans cette section



| Nom                                                               | Description                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------|
| [À propos des informations de version](about-version-information.md)         | Décrit les fonctions d’informations de version.<br/>            |
| [Utilisation des informations de version](using-version-information.md)         | Explique comment utiliser les fonctions d’informations de version.<br/> |
| [Informations de référence sur la version](version-information-reference.md) | Contient la référence de l’API.<br/>                             |



 

### <a name="version-information-functions"></a>Fonctions d’informations de version



| Nom                                                         | Description                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)             | Récupère des informations de version pour le fichier spécifié. <br/>                                                                                                                                                                                                                                                                                                     |
| [**GetFileVersionInfoEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoexa)         | Récupère des informations de version pour le fichier spécifié.<br/>                                                                                                                                                                                                                                                                                                      |
| [**Échec GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)     | Détermine si le système d’exploitation peut récupérer des informations de version pour un fichier spécifié. Si des informations de version sont disponibles, [**échec GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) retourne la taille, en octets, de ces informations. <br/>                                                                                                             |
| [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) | Détermine si le système d’exploitation peut récupérer des informations de version pour un fichier spécifié. Si des informations de version sont disponibles, [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) retourne la taille, en octets, de ces informations.<br/>                                                                                                          |
| [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)                           | Détermine l’emplacement d’installation d’un fichier selon qu’il localise ou non une autre version du fichier dans le système. Les valeurs [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) retournent dans les mémoires tampons spécifiées sont utilisées dans un appel ultérieur à la fonction [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) . <br/>                                                                          |
| [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)                     | Installe le fichier spécifié en fonction des informations retournées par la fonction [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) . [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) décompresse le fichier, si nécessaire, attribue un nom de fichier unique et recherche des erreurs, telles que des fichiers obsolètes. <br/>                                                                                   |
| [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)                   | Récupère une chaîne de description pour la langue associée à un identificateur de langage Microsoft binaire spécifié.<br/>                                                                                                                                                                                                                                          |
| [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)                       | Récupère les informations de version spécifiées à partir de la ressource d’informations de version spécifiée. Pour récupérer la ressource appropriée, avant d’appeler [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea), vous devez d’abord appeler la fonction [**échec GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) , puis la fonction [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) . <br/> |



 

### <a name="version-information-structures"></a>Structures d’informations de version



| Nom                                          | Description                                                                                                                                                                                                                      |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**String**](string-str.md)                  | Décrit l’Organisation des données dans une ressource de version de fichier. Elle contient une chaîne qui décrit un aspect spécifique d’un fichier, par exemple, la version d’un fichier, ses mentions de droits d’auteur ou ses marques.<br/>                |
| [**StringFileInfo**](stringfileinfo.md)      | Décrit l’Organisation des données dans une ressource de version de fichier. Elle contient des informations de version qui peuvent être affichées pour une langue et une page de codes particulières.<br/>                                                           |
| [**StringTable**](stringtable.md)            | Décrit l’Organisation des données dans une ressource de version de fichier. Elle contient des informations de mise en forme de la langue et de la page de codes pour les chaînes spécifiées par le membre **Children** . Une page de codes est un jeu de caractères ordonné.<br/> |
| [**Var**](var-str.md)                        | Décrit l’Organisation des données dans une ressource de version de fichier. Il contient généralement une liste de paires de langue et d’identificateur de page de codes que la version de l’application ou de la DLL prend en charge.<br/>                             |
| [**VarFileInfo**](varfileinfo.md)            | Décrit l’Organisation des données dans une ressource de version de fichier. Elle contient des informations sur la version qui ne dépendent pas d’une langue particulière et d’une combinaison de pages de codes.<br/>                                                        |
| [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) | Contient des informations sur la version d’un fichier. Ces informations sont indépendantes de la langue et de la page de codes. <br/>                                                                                                                   |
| [**VS \_ VERSIONINFO**](vs-versioninfo.md)     | Décrit l’Organisation des données dans une ressource de version de fichier. Il s’agit de la structure racine qui contient toutes les autres structures d’informations de version de fichier.<br/>                                                                    |



 

 

 





