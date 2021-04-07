---
title: Nouveautés (IMAPi)
description: Le tableau suivant identifie les nouveautés de chaque version de l’API de mastérisation d’image.
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77abc9db0c9d976eef632034a5620520bb29d73d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723827"
---
# <a name="whats-new-image-mastering-api"></a>Nouveautés : API de mastérisation d’images

Le tableau suivant identifie les nouveautés de chaque version de l’API de mastérisation d’image.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Version</th>
<th>Description des fonctionnalités</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Version 2.0</td>
<td>Une grande partie de l’API a été repensée. La plupart des fonctionnalités de la version 1,0 sont toujours disponibles dans la version 2,0. Ceux qui écrivent des applications de mastérisation d’image ou qui effectuent le développement de nouveaux appareils et formats sont encouragés à utiliser la version 2,0 au lieu de la version 1,0.<br/> IMAPi 2,0 est inclus dans Windows Vista. L’activation de la même fonctionnalité pour Windows XP et Windows Server 2003 requiert l’installation du package de mise à jour <a href="https://support.microsoft.com/kb/932716">KB932716</a> .<br/> Point-Release Remarques :<br/>
<ul>
<li>Une mise à jour offrant une prise en charge de plusieurs démarrages via l’interface <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a> a été introduite dans Windows Vista avec Service Pack 1 (SP1) et windows Server 2008.<br/></li>
<li>Une mise à jour de fonctionnalité offrant une prise en charge du contrôle du format BD-R\BD-RE, de la création d’une image CD-at-once, ainsi que de la vérification de la gravure, est incluse dans le <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Windows Feature Pack pour le stockage</a>. Cette mise à jour de fonctionnalité est prise en charge sur Windows Vista avec SP1, Windows XP avec Service Pack 2 (SP2) et versions ultérieures, et Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures. En outre, ces fonctionnalités sont incluses dans Windows 7 et Windows Server 2008.<br/></li>
<li>Les fonctionnalités IMAPi 2,0 natives à Windows 7 et Windows Server 2008 incluent la « ininterrompue brûlure » pour les CD audio et l’élimination de la « double dissimulation » lors des opérations de gravure. La double dissimulation est un processus, au sein d’une opération de gravure plus large, dans laquelle chaque fichier est recherché avant d’être gravé sur le disque. Avec la dernière version d’IMAPi 2,0, les fichiers sont choisis de manière sélective pour la dissimulation, laissant les fichiers restants (principalement des fichiers volumineux) non dissimulés. Le résultat final est l’espace disque et l’heure de l’opération enregistrés.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Version 1.0</td>
<td>Version initiale. Permet à une étape de l’application et de graver une image audio ou de données simple sur des périphériques CD-R et CD-RW. L’API prend en charge les formats Joliet et ISO 9660 pour les disques de données et audio Redbook. Pour plus d’informations sur la version 1,0, consultez <a href="imapiv1.md">prise en charge de IMAPIv1</a>. Inclus dans Windows XP.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="version-20"></a>Version 2.0

-   Permet aux applications d’effectuer des gravures sur les formats DVD-R, DVD + R, DVD-RW, DVD + RW, DVD + DL, DVD-DL, DVD-RAM, BD-R et BD-RE.
-   Autorise l’enregistrement sur plusieurs lecteurs en même temps. Dans la version 1,0, un seul enregistreur sur le système peut être utilisé par IMAPi à un moment donné. Si vous exécutez une application version 1,0 sur Windows Vista, d’autres applications peuvent utiliser simultanément les interfaces IMAPi 1,0 ou 2,0 sur d’autres lecteurs du système. Bien que cette opération soit généralement considérée comme un avantage, les applications qui reposent sur le comportement du graveur de système unique peuvent nécessiter des mises à jour mineures.
-   L’accès à un enregistreur est refusé lorsque l’enregistreur écrit des informations sur le disque. Dans le cas contraire, l’enregistreur est disponible pour d’autres clients.
-   Prend en charge plusieurs fichiers de dissimulation sur un ordinateur client, tandis que la version 1,0 n’autorise qu’un seul fichier de dissimulation à l’ensemble du système.
-   Sur Windows Vista, la version 1,0 ne contient plus de composants de service ou de mode noyau. Toutefois, l’interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) utilise toujours l' \_ accès exclusif du cdrom IOCTL et le \_ \_ transfert IOCTL \_ SCSI via des \_ \_ \_ commandes directes pour gérer l’accès ou la communication à des périphériques de lecteur spécifiques.
-   Sur Windows Vista, les interfaces de la version 1,0 appellent désormais les interfaces de la version 2,0.
-   Inclus avec Windows Vista avec SP1 et Windows Server 2008, IMAPi requise 2,0 offre une prise en charge du démarrage multiple via l’interface [**IFileSystemImage2**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2) .
-   Autorise l’utilisation de « ininterrompue Burning » pour les CD audio. Avec la gravure ininterrompue, le décalage audible entre les pistes audio peut être supprimé.
-   Remplacement de la « double dissimulation » par un processus qui sélectionne spécifiquement des fichiers pour la dissimulation et laisse les fichiers restants (principalement des fichiers volumineux) non dissimulés. Le résultat final est l’espace disque et l’heure de l’opération enregistrés.
-   Avec le [Pack de fonctionnalités Windows pour le stockage](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05), les options de vérification de la gravure ont été mises à disposition avec une propriété accessible via [**IBurnVerification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification).
