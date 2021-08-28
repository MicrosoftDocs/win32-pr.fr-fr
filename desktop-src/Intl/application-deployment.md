---
description: Cette section décrit les considérations relatives au déploiement de votre application MUI pour une utilisation optimale par la logique de chargement de l’application et le chargeur de ressources.
ms.assetid: 6c10b355-9bdd-4dba-8446-91034d4fe9b8
title: Déploiement d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f297767c2b22fb8a3096f0df8ed21468ab710
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883518"
---
# <a name="application-deployment"></a>Déploiement d’application

Cette section décrit les considérations relatives au déploiement de votre application MUI pour une utilisation optimale par la logique de chargement de l’application et le chargeur de ressources.

## <a name="packaging"></a>Packaging

l’empaquetage de l’application dépend du type de prise en charge linguistique fourni, comme Windows installe les modules linguistiques en fonction des préférences de l’utilisateur. Par exemple, si vous avez décidé de prendre en charge les paramètres de langue du système, vous souhaiterez peut-être fournir la prise en charge linguistique dans un package unique, quel que soit l’utilisateur prévu.

Si l’application et les ressources sont volumineuses, vous devez utiliser un package par langue prise en charge. Par exemple, vous pouvez utiliser ce type de Packaging si votre application présente des langues sélectionnables par l’utilisateur et si l’utilisateur a besoin de l’ajout et de la suppression dynamiques des ressources de langue.

## <a name="file-placement-on-windows-vista-and-later"></a>emplacement des fichiers sur Windows Vista et versions ultérieures

cette section décrit l’emplacement des fichiers pour une application MUI ciblée uniquement sur Windows Vista et versions ultérieures.

### <a name="place-the-ln-file"></a>Placez le fichier LN

Un fichier LN standard pour une application MUI est un fichier .exe ou un fichier .dll, par exemple BakerDelta.dll. Vous devez placer ce fichier dans le dossier racine dans lequel votre application est installée, par exemple, X : \\ \\ &lt; somepath &gt; \\BakerDelta.dll.

### <a name="place-language-specific-resource-files"></a>Placer Language-Specific fichiers de ressources

Vos fichiers de ressources spécifiques à une langue doivent avoir des noms prévisibles formés en ajoutant « . mui » au nom complet du fichier LN, par exemple, BakerDelta.dll. mui. Ces fichiers doivent être placés dans des sous-dossiers nommés d’après les [noms de langue](language-names.md)appropriés. L’exemple suivant montre le placement des ressources pour le fichier BakerDelta.dll LN, avec les fichiers de ressources spécifiques à la langue pour l’anglais (Royaume-Uni), l’anglais (États-Unis), l’anglais neutre, l’espagnol (Espagne), l’espagnol (Mexique) et l’espagnol neutre :

-   X : \\ \\ &lt; somepath &gt; \\BakerDelta.dll
-   X : \\ \\ &lt; somepath &gt; \\ en Go \\BakerDelta.dll. mui
-   X : \\ \\ &lt; somepath &gt; \\ en-US \\BakerDelta.dll. mui
-   X : \\ \\ &lt; somepath en &gt; \\ \\BakerDelta.dll. mui
-   X : \\ \\ &lt; somepath &gt; \\ es-es \\BakerDelta.dll. mui
-   X : \\ \\ &lt; somepath &gt; \\ es-MX \\BakerDelta.dll. mui
-   X : \\ \\ &lt; somepath &gt; \\ es \\BakerDelta.dll. mui

Les fichiers de ressources doivent être placés dans leurs emplacements corrects lors de l’installation de l’application MUI ou d’un package de langue. Il est important de placer chaque fichier dans le dossier approprié, car le chargeur de ressources ne peut pas fonctionner correctement dans le cas contraire. À l’aide de l’exemple ci-dessus, le chargeur de ressources examine X : \\ &lt; somepath &gt; \\ en-US \\BakerDelta.dll. mui pour les ressources en anglais (États-Unis). Si le chargeur examine ce fichier et rencontre uniquement des ressources de langue espagnole, il échoue.

## <a name="file-placement-on-a-pre-windows-vista-operating-system"></a>emplacement des fichiers sur un système d’exploitation antérieur à Windows Vista

une application à exécuter sur un système d’exploitation pré-Windows vista peut utiliser la convention Windows Vista de placement de fichiers de ressources spécifiques à une langue dans des dossiers basés sur les noms de langue. L’application peut également se conformer à une Convention plus ancienne qui forme des chemins d’accès à partir d' [identificateurs de langue](language-identifiers.md). Pour les applications qui ne prennent en charge qu’une seule langue, vous pouvez simplement placer le fichier de ressources spécifique au langage dans le répertoire racine avec le fichier binaire.

Par exemple, considérez un fichier LN appelé BakerDelta.dll, avec des fichiers de ressources spécifiques à la langue pour l’anglais (Royaume-Uni), l’anglais (États-Unis), l’anglais neutre, l’espagnol (Espagne), l’espagnol (Mexique) et l’espagnol neutre. une installation sur un système d’exploitation pré-Windows Vista peut placer ces fichiers comme suit :

-   X : \\ \\ &lt; somepath &gt; \\BakerDelta.dll
-   X : \\ \\ &lt; somepath &gt; \\BakerDelta.dll. mui (fichier. mui facultatif contenant les ressources dans la langue du système d’exploitation en tant que solution de secours ultime)
-   X : \\ \\ &lt; somepath &gt; \\ MUI \\ 0809 \\BakerDelta.dll. mui
-   X : \\ \\ &lt; somepath &gt; \\ MUI \\ 0409 \\BakerDelta.dll. mui
-   X : \\ \\ &lt; somepath &gt; \\ MUI \\ 0209 \\BakerDelta.dll. mui
-   X : \\ \\ &lt; somepath &gt; \\ MUI \\ 040a \\BakerDelta.dll. mui
-   X : \\ \\ &lt; somepath &gt; \\ MUI \\ 080a \\BakerDelta.dll. mui
-   X : \\ \\ &lt; somepath &gt; \\ MUI \\ 0209 \\BakerDelta.dll. mui

En plus de ces fichiers, l’application peut configurer un fichier de ressources de langue de secours ultime, afin de résider dans le même dossier que l’application elle-même. Dans l’exemple ci-dessus, le fichier est X : \\ &lt; somepath &gt; \\BakerDelta.dll. mui.

## <a name="installation"></a>Installation

La logique d’installation pour copier et configurer des fichiers d’application repose sur les langues prises en charge et sur l’emplacement des fichiers de ressources de langue dans les emplacements d’installation appropriés. Un programme d’installation doit installer et configurer l’application afin que l’utilisateur puisse facilement ajouter et supprimer des langues.

Si votre application installe simplement la langue du système d’exploitation cible, le programme d’installation doit détecter l’interface utilisateur du système d’exploitation pour déterminer les ressources d’application à installer. Pour prendre en charge la meilleure expérience utilisateur, le programme d’installation doit également détecter la langue de l’interface utilisateur pour présenter une interface utilisateur localisée pour l’installation elle-même.

il est recommandé d’utiliser Windows Installer (MSI) pour créer votre logiciel d’installation. Les ressources associées doivent être incluses dans le fichier de ressources de la langue de base, comme décrit dans [création du fichier de ressources de la langue de base](creating-the-base-language-resource-file.md). pour obtenir des instructions sur l’utilisation de MSI pour préparer le programme d’installation de l’application, consultez [Windows Installer](../msi/windows-installer-portal.md).

## <a name="uninstall-program"></a>Désinstaller le programme

Vous pouvez également souhaiter fournir un programme de désinstallation avec votre application MUI. MSI est également recommandé pour la création de ce programme. pour obtenir des instructions sur l’utilisation de MSI pour préparer le logiciel de désinstallation, consultez [Windows Installer](../msi/windows-installer-portal.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation de interface utilisateur multilingue](using-multilingual-user-interface.md)
</dt> </dl>

 

 
