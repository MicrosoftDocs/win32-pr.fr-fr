---
description: à partir de Windows Installer&\# 160 ; version&\# 160 ; 3.0, il est possible de créer et d’installer des correctifs qui peuvent être désinstallés séparément et dans n’importe quel ordre, sans avoir à désinstaller et réinstaller l’application entière et les autres correctifs.
ms.assetid: 2ad30ac9-eac9-49cf-98ae-5c053a0b500a
title: Suppression des correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd54db3bde3a356a0c3adb299555248bbc87a0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195355"
---
# <a name="removing-patches"></a>Suppression des correctifs

à partir de Windows Installer version 3,0, il est possible de créer et d’installer des correctifs qui peuvent être désinstallés séparément et dans n’importe quel ordre, sans avoir à désinstaller et réinstaller l’application entière et les autres correctifs. Windows Le programme d’installation 3,0 permet également de créer des [packages de correctifs](patch-packages.md) à l’aide d’une [table MsiPatchSequence](msipatchsequence-table.md) contenant des informations sur le séquencement des correctifs. avec les versions de Windows Installer antérieures à Windows Installer 3,0, la seule méthode permettant de supprimer des correctifs particuliers d’une application consiste à désinstaller l’ensemble de l’application corrigée, puis à réinstaller sans réappliquer les correctifs en cours de suppression.

le fait de pouvoir désinstaller un correctif dépend de la manière dont le correctif a été créé, de la version de Windows Installer utilisée pour installer le correctif et des modifications apportées par le correctif à l’application. Si un correctif ne peut pas être installé, le seul moyen de supprimer le correctif consiste à désinstaller l’application entière et à la réinstaller sans appliquer le correctif en cours de suppression.

Vous pouvez désinstaller un ou plusieurs correctifs à l’aide d’une option de ligne de commande, de l’interface de script ou en appelant [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) à partir d’une autre application. Pour plus d’informations sur la désinstallation des correctifs, voir [désinstallation des correctifs](uninstalling-patches.md) .

La valeur de la propriété [**MSIPATCHREMOVE**](msipatchremove.md) répertorie les correctifs à désinstaller. Pour chaque correctif de la liste, le programme d’installation vérifie que le correctif n’est pas installé. Si l’utilisateur ne dispose pas des privilèges nécessaires pour supprimer le correctif, si le correctif est inconnu pour le produit, si la stratégie de correctifs empêche la suppression ou si le correctif a été marqué comme ne pouvant pas être installé, le programme d’installation renvoie une erreur indiquant qu’une transaction d’installation a échoué. Pour plus d’informations sur les éléments qui déterminent si un correctif ne peut pas être installé, consultez [correctifs non installés](uninstallable-patches.md) .

Une fois que le correctif est vérifié comme étant amovible, le programme d’installation supprime le correctif de la séquence d’application du correctif. pour plus d’informations sur la façon dont Windows Installer 3,0 détermine la séquence à utiliser lors de l’application des correctifs, consultez mise en [séquence des correctifs](sequencing-patches.md). Notez que la suppression de correctifs de la séquence peut entraîner la désactivation des correctifs marqués comme obsolètes ou remplacés.

Tous les correctifs sélectionnés pour la suppression sont répertoriés dans la propriété [**MsiPatchRemovalList**](msipatchremovallist.md) . Cette propriété est une propriété privée qui est définie par le programme d’installation et peut être utilisée dans les expressions conditionnelles ou interrogée par des [actions personnalisées](custom-actions.md). La propriété contient la liste des GUID de code correctif des correctifs à supprimer. Une action personnalisée peut déterminer si l’état d’installation du correctif est appliqué, obsolète ou remplacé en appelant la propriété [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) ou [**PatchProperty**](patch-patchproperty.md) de l' [objet patch](patch-object.md).

Après la suppression d’un correctif, l’état de l’application est le même que si le correctif n’a jamais été installé. Si possible, le programme d’installation limite le processus au sous-ensemble de fonctionnalités affectées par le correctif en cours de suppression. Le programme d’installation définit automatiquement la propriété [**réinstaller**](reinstall.md) sur la liste des fonctionnalités affectées. Les fichiers qui ont été ajoutés par le correctif sont supprimés et les fichiers qui ont été modifiés par le correctif sont remplacés. Les fichiers et les entrées de Registre sont restaurés à la version attendue par le produit moins le correctif. Les fonctionnalités et les composants qui ont été ajoutés par le correctif sont désinscrits de l’application. Notez que le contenu supplémentaire ajouté par le correctif peut rester sur l’ordinateur de l’utilisateur si le contenu est utilisé par un autre correctif qui est toujours applicable.

Si un fichier d’un composant partagé est mis à jour par un correctif, la modification affecte toutes les applications qui partagent le composant. Une fois le correctif supprimé, la modification affecte toutes les applications qui partagent le composant. Cela signifie que la suppression d’un correctif par une application peut restaurer le fichier du composant partagé dans une version inférieure à celle requise par une autre application. Cela peut corriger la première application, mais provoquer l’arrêt du fonctionnement de la deuxième application. Dans ce cas, la deuxième application peut être réparée en réinstallant la deuxième application à l’aide des méthodes décrites dans [réinstallation d’une fonctionnalité ou d’une application](reinstalling-a-feature-or-application.md). Cette opération restaure la version corrigée du fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Séquencement des correctifs](sequencing-patches.md)
</dt> <dt>

[Actions personnalisées de désinstallation des correctifs](patch-uninstall-custom-actions.md)
</dt> <dt>

[Correctifs désinstallés](uninstallable-patches.md)
</dt> <dt>

[Désinstallation des correctifs](uninstalling-patches.md)
</dt> </dl>

 

 



