---
description: Une étiquette est un nom convivial qui est affecté à un volume, généralement par un utilisateur final, pour faciliter sa reconnaissance. Un volume peut avoir une étiquette, une lettre de lecteur, les deux ou aucune des deux. Pour définir l’étiquette d’un volume, utilisez la fonction SetVolumeLabel.
ms.assetid: f640f42d-a703-4e2e-a6d3-09cbe989cd11
title: Attribution d’un nom à un volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6435b6b5c7283cf2fb9a98951698f79646dfdffa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009897"
---
# <a name="naming-a-volume"></a>Attribution d’un nom à un volume

Une étiquette est un nom convivial qui est affecté à un volume, généralement par un utilisateur final, pour faciliter sa reconnaissance. Un volume peut avoir une étiquette, une lettre de lecteur, les deux ou aucune des deux. Pour définir l’étiquette d’un volume, utilisez la fonction [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .

Plusieurs facteurs peuvent compliquer l’identification de volumes spécifiques en utilisant uniquement des lettres de lecteur et des étiquettes. L’une d’elles est qu’un volume n’a pas besoin d’une lettre de lecteur ou d’une étiquette. Un autre est que deux volumes différents peuvent avoir la même étiquette, ce qui les rend indifférenciables, sauf par lettre de lecteur. Un troisième facteur est que les attributions de lettres de lecteur peuvent changer à mesure que des volumes sont ajoutés et supprimés de l’ordinateur.

Pour résoudre ce problème, le système d’exploitation utilise des *chemins d’accès de GUID de volume* pour identifier les volumes. Il s’agit de chaînes de ce format :

"\\\\?\\ Volume {*GUID*} \\ »

où *GUID* est un identificateur global unique (Guid) qui identifie le volume.

Un chemin d’accès de GUID de volume est parfois appelé *nom de volume unique*, car un chemin d’accès de GUID de volume ne peut faire référence qu’à un seul volume. Toutefois, ce terme est trompeur, car un volume peut avoir plus d’un chemin d’accès de GUID de volume.

Le \\ \\ \\ préfixe «  ? » désactive l’analyse du chemin d’accès et n’est pas considéré comme faisant partie du chemin d’accès. Pour plus d’informations sur le \\ \\ \\ préfixe «  ? », consultez [attribution d’un nom à un fichier ou à un répertoire](naming-a-file.md).

Vous devez spécifier des chemins d’accès complets lorsque vous utilisez des chemins d’accès de GUID de volume avec le \\ \\ \\ préfixe «  ? ».

Un *dossier monté* est une association entre un dossier sur un volume et un autre volume, de sorte que le chemin d’accès au dossier puisse être utilisé pour accéder au volume. Par exemple, si vous utilisez la fonction [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) pour créer un dossier monté qui associe le volume « d : \\ » au dossier « c : \\ Mounted \\ », vous pouvez utiliser l’un ou l’autre chemin d’accès (« d : \\ » ou « c : \\ Mounted \\ ») pour accéder au volume « D : \\ ».

Un *point de montage de volume* est un chemin de mode utilisateur qui peut être utilisé pour accéder à un volume. Il existe trois types de points de montage de volume :

-   Une lettre de lecteur, par exemple, « C : \\ ».
-   Un chemin d’accès de GUID de volume, par exemple, « \\ \\ ? \\ Volume {26a21bda-A627-11D7-9931-806e6f6e6963} \\ ».
-   Un dossier monté, par exemple, « C : \\ Mounted \\ ».

Toutes les fonctions de volume et de dossier monté qui prennent un chemin d’accès de GUID de volume comme paramètre d’entrée nécessitent la barre oblique inverse de fin. Toutes les fonctions de volume et de dossier monté qui retournent un chemin d’accès de GUID de volume fournissent la barre oblique inverse de fin, mais ce n’est pas le cas avec la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Vous pouvez ouvrir un volume en appelant **CreateFile** et omettre la barre oblique inverse à la fin du nom de volume que vous spécifiez. **CreateFile** traite un chemin d’accès de GUID de volume avec une barre oblique inverse ajoutée comme répertoire racine du volume.

Le système d’exploitation affecte un chemin d’accès au GUID du volume à un volume lorsque le volume est installé pour la première fois et lorsque le volume est formaté. Les fonctions de volume et de dossier monté utilisent des chemins d’accès de GUID de volume pour accéder aux volumes. Pour obtenir le chemin d’accès du GUID du volume d’un volume, utilisez la fonction [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .

Les longueurs de chemins peuvent être un problème lors de la création d’un dossier monté qui associe un volume comportant une arborescence de répertoires profonde à un répertoire situé sur un autre volume. Cela est dû au fait que le chemin d’accès du volume est concaténé au chemin d’accès du répertoire. Le **\_ chemin d’accès maximal** de constante définie globalement définit le nombre maximal de caractères qu’un chemin d’accès peut avoir. (Pour plus d’informations sur le **\_ chemin d’accès maximal**, consultez [attribution d’un nom à un fichier ou à un répertoire](naming-a-file.md).) Vous pouvez éviter cette contrainte en procédant de l’une des façons suivantes :

-   Reportez-vous aux volumes par leurs chemins d’accès de GUID de volume.
-   Utilisez les versions Unicode (W) des fonctions de fichier qui prennent en charge le \\ \\ \\ préfixe ?.

 

 



