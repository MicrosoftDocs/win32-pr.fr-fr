---
description: le composant Microsoft Windows Journal Note Reader fournit un accès par programmation aux fichiers au format journal.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Utilisation du composant de lecture du journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41559ac31ff081ecb810b0fe6e82ce1107ed87dae897cc7e6b8be4569e9b78f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449188"
---
# <a name="using-the-journal-reader-component"></a>Utilisation du composant de lecture du journal

le composant Microsoft Windows Journal Note Reader fournit un accès par programmation aux fichiers au format journal.

## <a name="component-overview"></a>Vue d’ensemble des composants

Les fichiers journaux ont l’extension de fichier. jnt. Ce composant simple prend un flux contenant un fichier. jnt et retourne un flux contenant le contenu du fichier au format XML. Le code XML retourné par le composant est conforme au schéma du lecteur de note du journal. Ce schéma est documenté dans [Référence du schéma du lecteur du journal](journal-reader-schema-reference.md).

Le composant ne permet pas d’écrire des fichiers. jnt.

Le composant est disponible dans les versions managées et non managées. Le composant non managé est disponible dans la bibliothèque de liens dynamiques (DLL) journal.dll. la version managée se trouve dans l’assembly Microsoft.Ink.Journal.dll (pour la redistribution vers Windows XP édition Tablet PC ou Windows Vista), ou Microsoft.Ink.dll.

> [!IMPORTANT]
>
> à partir de Windows 10, la version 1607, journal.dll n’est pas inclus dans le système d’exploitation Windows. Cette bibliothèque doit être considérée comme dépréciée ou obsolète et ne doit pas être utilisée.

 

### <a name="assembly-changes-of-note"></a>Modifications de l’assembly de note

il est important de tenir compte de certaines modifications apportées à l’assembly contenant le composant lecteur de Note de Journal qui s’est produit entre la version publiée avec la version 1,7 du Kit de développement de Tablet pc et la version fournie avec le système d’exploitation Windows Vista.

la version 1,7 du composant lecteur, qui peut être redistribuée vers Windows XP ou Windows Vista, est contenue dans un assembly appelé Microsoft.Ink.Journal.dll. le composant lecteur est fourni avec Windows Vista, mais il a été intégré à l’assembly Microsoft.Ink.dll principal. Cela signifie que les applications qui utilisent l’assembly 1,7 doivent redistribuer cet assembly avec leur installation.

## <a name="using-the-component"></a>Utilisation du composant

Le composant lecteur de note de journal est utile pour extraire les données d’entrée manuscrite et d’autres informations sur le fichier à partir d’un fichier journal.

### <a name="com"></a>COM

Le composant COM lecteur de note de journal se trouve dans le fichier Journal.dll, qui est installé et inscrit lorsque vous téléchargez et exécutez le fichier d’installation du lecteur de note de journal.

Le composant COM ne prend pas en charge l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .

### <a name="managed"></a>Adresses IP gérées

Le composant géré du lecteur de note de journal se trouve dans l’assembly de Microsoft.Ink.JournalReader.dll. Cet assembly est installé et inscrit dans le Global Assembly Cache lorsque vous exécutez le fichier d’installation du lecteur de note de journal.

Ajoutez une référence à l’assembly pour l’utiliser dans votre projet managé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IJournalReader**](ijournalreader.md)
</dt> <dt>

[Référence du schéma du lecteur de journal](journal-reader-schema-reference.md)
</dt> </dl>

 

 
