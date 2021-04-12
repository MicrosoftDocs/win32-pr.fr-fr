---
title: Nouveautés (BITS)
description: Le tableau suivant identifie les nouveautés de chaque version de Service de transfert intelligent en arrière-plan (BITS).
ms.assetid: ef05f2e1-88be-4adb-aca7-a7b1451cfd04
keywords:
- Nouveautés (BITS)
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b171a1d8cede9e3fd49ac81ab47ffb09f72b6200
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032173"
---
# <a name="whats-new-bits"></a>Nouveautés (BITS)

Depuis sa première publication dans le cadre de Windows XP, le Service de transfert intelligent en arrière-plan (BITS) a été constamment amélioré, ce qui ajoute des contrôles plus puissants au développeur et à l’administrateur pour contrôler et gérer les téléchargements. Un ensemble complet d’applets de commande PowerShell a été ajouté. Il peut se connecter à plusieurs types de serveurs HTTP ; Il est plus prudent de la bande passante réseau de l’utilisateur et des coûts qu’auparavant. 

Le tableau suivant identifie les nouveautés de chaque version de Service de transfert intelligent en arrière-plan (BITS).



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
<td>Version 10,3</td>
<td>Nouvelles fonctionnalités :<br/>
<ul>
<li>Ajout de <a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>BackgroundCopyJobHttpOptions3</strong></a> pour marquer les en-têtes HTTP en écriture seule et pour définir un rappel de validation de certificat de serveur.</li>
<li>BITS conserve son identité de service lorsqu’il est créé par un autre service système.</li>
<li>Le service BITS continue de transférer les fichiers sur la veille connectée tant que l’appareil est branché.</li>
</ul>
La version de BITS 10,3 est incluse dans la mise à jour de Windows 10 mai 2019 (10,0 ; Build 18362) et versions ultérieures.
</td>
</tr>
<tr class="even">
<td>Version 10,2</td>
<td>Nouvelles fonctionnalités :<br/>
<ul>
<li>Ajout de <a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>BackgroundCopyJobHttpOptions2</strong></a> pour modifier la méthode http pour les téléchargements http.</li>
<li>BITS utilise désormais le classement par défaut du proxy pour être plus cohérent avec le reste du système.</li>
<li>Il est plus facile pour les programmeurs de définir la configuration du proxy BITS pour les scénarios d’entreprise.</li>
<li>Le service BITS est désormais plus attentif à la puissance et prend en charge la [mise en veille moderne](/windows-hardware/design/device-experiences/modern-standby).</li>
<li>BITS prennent désormais en charge les [stratégies](/windows/client-management/mdm/policy-configuration-service-provider) de gestion des appareils mobiles (MDM) en plus des [stratégies de groupe](./group-policies).</li>
</ul>
La version de BITS 10,2 est incluse dans la mise à jour 2018 d’octobre de Windows 10 (10.0 ; Build 17763) et versions ultérieures.
</td>
</tr>
<tr class="odd">
<td>Version 10,1</td>
<td>Nouvelles fonctionnalités :<br/>
<ul>
<li>Ajout de <a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6</strong></a> et <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>IBackgroundCopyCallback3</strong></a> pour activer les scénarios d’accès aléatoire pour les téléchargements http.</li>
<li>Ajout de <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> et <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> à l’énumération <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a> pour ajuster les comportements de téléchargement et de notification, respectivement.</li>
</ul>
La version de BITS 10,1 est incluse dans la mise à jour de Windows 10 Creator et versions ultérieures.
</td>
</tr>
<tr class="even">
<td>Version 5.0</td>
<td>Nouvelles fonctionnalités :<br/>
<ul>
<li>Ajout de l’interface <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> qui ajoute des méthodes génériques pour obtenir et définir les propriétés des tâches bits sur les méthodes héritées de l’interface <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>IBackgroundCopyJob4</strong></a> .<br/> Pour plus d’informations sur l’utilisation de la nouvelle interface <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> , consultez <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">Comment contrôler si un travail bits est autorisé à être téléchargé sur une connexion coûteuse</a> et <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">Comment obtenir le dernier jeu d’en-têtes http reçu pour chaque fichier dans un travail de téléchargement bits</a>.<br/></li>
<li>Ajout de l’Union <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>BITS_JOB_PROPERTY_VALUE</strong></a> et des énumérations de <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a>et de <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>BITS_JOB_TRANSFER_POLICY</strong></a> . Pour obtenir des exemples d’utilisation, consultez les rubriques ci-dessus.</li>
<li>Ajout de l’interface <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> , qui ajoute des méthodes pour obtenir et définir des propriétés génériques sur les objets BackgroundCopyFile aux méthodes héritées de l’interface <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>IBackgroundCopyFile4</strong></a> . L’ajout de propriétés génériques permet d’améliorer les fonctionnalités de BackgroundCopyFile à l’avenir sans nécessiter la création d’une nouvelle interface.</li>
<li>La première propriété générique exposée par <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> est la propriété <strong>HttpResponseHeaders</strong> .</li>
<li>Ajout de l' <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>BITS_FILE_PROPERTY_VALUE</strong></a> Union et de l’énumération <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>BITS_FILE_PROPERTY_ID</strong></a> .</li>
</ul>
La version de BITS 5,0 est incluse dans les systèmes d’exploitation Windows Server 2012 et Windows 8, où la version de% windir% \System32\QMgr.dll est &quot; 7.7. xxxx. xxxx &quot; .<br/> Les fonctionnalités suivantes ont été ajoutées à BITS dans Windows 10<br/>
<ul>
<li>Dans Windows 10, version 1607, il est possible d’utiliser les API COM BITS et les applets de commande PowerShell BITS (le cas échéant) dans une session à distance PowerShell. Cela s’avère particulièrement utile lorsque vous administrez des versions de Windows Server 2016 qui n’ont pas de fonctionnalité de connexion locale. Les tâches BITS démarrées via les sessions PowerShell à distance s’exécutent dans le contexte de compte de l’utilisateur de la session et progresseront uniquement quand au moins une ouverture de session locale sera active ou une session PowerShell à distance sera associée à ce compte d’utilisateur. Envisagez d’utiliser des sessions à distance PowerShell persistantes (voir <a href="/powershell/module/microsoft.powershell.core/new-pssession">New-PSSession</a>) pour les transferts à long terme.</li>
<li>Dans Windows 10, la version 1607, il est désormais possible pour un propriétaire de tâche BITS de définir des jetons d’assistance sans être administrateur, tant que le jeton d’assistance ne dispose pas de fonctionnalités d’administrateur. Cela réduit l’espace de vulnérabilité des outils de mise à jour ou de téléchargement en arrière-plan en leur permettant de s’exécuter sur le compte NetworkService avec le moins de privilèges plutôt que sur un compte doté de privilèges administrateur.</li>
</ul>
La version de BITS 5,0 est également incluse dans Windows 10, où la version de% windir% \System32\QMgr.dll est &quot; 7,8. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Version 4.0</td>
<td>Nouvelles fonctionnalités :<br/>
<ul>
<li>La mise en cache d’homologue utilise désormais Windows BranchCache. Ce nouveau modèle de mise en cache d’homologue remplace le modèle utilisé pour la version de BITS 3,0. Pour plus d’informations, consultez <a href="peer-caching.md">mise en cache d’homologue</a>.</li>
<li>Ajout d’un modèle d’accès aux ressources plus flexible qui permet aux applications d’associer une paire de jetons de sécurité à une tâche de transfert BITS. Pour plus d’informations, consultez <a href="helper-tokens-for-bits-transfer-jobs.md">jetons d’assistance pour les tâches de transfert bits</a>.</li>
<li>Ajout de <a href="bits-compact-server.md">bits Compact Server</a>, un serveur de fichiers HTTP/HTTPS autonome qui permet de transférer un nombre limité de fichiers volumineux de manière asynchrone entre les ordinateurs.</li>
<li>Ajout d’une limitation de bande passante plus granulaire. Pour plus d’informations, consultez <a href="group-policies.md">stratégies de groupe</a>.</li>
</ul>
La version de BITS 4,0 est incluse dans les systèmes d’exploitation Windows Server 2008 R2 et Windows 7.<br/> Vous pouvez également télécharger BITS 4,0 pour Windows Server 2008 avec Service Pack 2 (SP2), Windows Vista avec Service Pack 1 (SP1) et Windows Vista avec Service Pack 2 (SP2). Pour plus d’informations sur le téléchargement de BITS 4,0, consultez <a href="https://support.microsoft.com/kb/968929">l’article KB968929</a>.<br/> La version de% windir% \System32\QMgr.dll est &quot; 7.5. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Version 3.0</td>
<td>Nouvelles fonctionnalités :<br/>
<ul>
<li>Ajout de <a href="peer-caching.md">la mise en cache d’homologue</a> qui vous permet de télécharger du contenu à partir d’homologues et de fournir du contenu à des pairs dans un réseau de domaine.</li>
<li>Ajout d’une <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">notification</a> lors du téléchargement d’un fichier.</li>
<li>Accès au <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">fichier temporaire</a> ajouté pendant la progression du téléchargement.</li>
<li>Ajout de la possibilité de contrôler les <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">redirections</a>http.</li>
<li>Ajout de <a href="group-policies.md">stratégies de groupe</a> supplémentaires pour contrôler la mise en cache d’homologue et limiter les temps de téléchargement.</li>
<li>Ajout des événements de diagnostic et de dépannage dans le journal des événements système.</li>
<li>Ajout de la prise en charge du <a href="user-account-control-and-bits.md">contrôle de compte d’utilisateur</a> (UAC).</li>
<li>Sur Windows Vista et versions ultérieures, le type de démarrage BITS par défaut est le démarrage automatique différé.</li>
</ul>
<blockquote>
[!Note]<br />
BITS utilise désormais des stratégies de groupe pour limiter le nombre de travaux et de fichiers que vous pouvez créer. Cela peut affecter les applications qui créent actuellement un grand nombre de travaux ou ajouter un grand nombre de fichiers à un travail.
</blockquote>
<br/> <br/> La version de BITS 3,0 est incluse dans les systèmes d’exploitation Windows Server 2008 et Windows Vista. <br/> La version de% windir% \System32\QMgr.dll est &quot; 7.0. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Version 2.5</td>
<td>Ajout de la prise en charge des en-têtes HTTP personnalisés, de l’authentification du client basé sur les certificats pour les transports HTTP sécurisés et IPv6. Ajout également des compteurs IGD (Internet Gateway Device) pour calculer plus précisément la <a href="network-bandwidth.md">bande passante</a>disponible.<br/> Les fonctionnalités BITS 2,5 sont disponibles dans les systèmes d’exploitation Windows Server 2008, Windows Vista et Windows XP avec Service Pack 3 (SP3). <br/> Vous pouvez également télécharger BITS 2,5 pour Windows Server 2003 avec Service Pack 2 (SP2), Windows Server 2003 avec Service Pack 1 (SP1) et Windows XP avec Service Pack 2 (SP2). Pour télécharger BITS 2,5, accédez au <a href="https://www.microsoft.com/download/details.aspx?id=4933">Centre de téléchargement Microsoft</a> et installez KB923845.<br/> La version de% windir% \System32\QMgr.dll est &quot; 6.7. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Version 2.0</td>
<td>Ajout de la prise en charge de l’exécution de téléchargements de premier plan simultanés, à l’aide de chemins d’accès SMB (Server Message Block) pour les noms distants, en téléchargeant des plages d’un fichier, en modifiant le préfixe ou le nom complet d’un nom distant, et en limitant l’utilisation La stratégie paramètre jobinactivitytimeout se trouve maintenant sous Configuration ordinateur, Modèles d’administration, réseau, Service de transfert intelligent en arrière-plan (BITS).<br/> La version de BITS 2,0 est incluse dans Windows XP avec SP2 et Windows Server 2003 avec SP1. Vous pouvez également télécharger BITS 2,0 pour Windows Server 2003 et Windows XP. Pour télécharger BITS 2,0, accédez au <a href="https://www.microsoft.com/download/details.aspx?id=19031">Centre de téléchargement Microsoft</a> et installez KB842773.<br/> La version de% windir% \System32\QMgr.dll est &quot; 6.6. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Version 1.5</td>
<td>Ajout de la fonctionnalité de chargement et de chargement-réponse, de l’exécution de la ligne de commande pour les événements, des informations d’identification explicites et des informations d’identification du proxy.<br/> À partir de BITS 1,5, les utilisateurs disposant d’un <a href="/windows/win32/secauthz/restricted-tokens">jeton restreint</a> ne peuvent pas créer ou modifier des travaux.<br/> La version de BITS 1,5 est incluse dans Windows Server 2003. Un package redistribuable est disponible pour Windows XP à partir du <a href="https://www.microsoft.com/download/details.aspx?id=22250">Centre de téléchargement Microsoft</a>.<br/> La version de% windir% \System32\QMgr.dll est &quot; 6.5. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Version 1.2</td>
<td>Mêmes fonctionnalités que la version 1,0. Contient des améliorations et des mises à niveau internes.<br/> La version de BITS 1,2 est incluse dans Windows XP avec Service Pack 1 (SP1).<br/> La version de% windir% \System32\QMgr.dll est &quot; 6.2. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Version 1.0</td>
<td>Version initiale. Fournit des téléchargements hiérarchisés, limités et asynchrones en arrière-plan ou au premier plan. Les téléchargements reprennent automatiquement après le redémarrage de l’ordinateur et la déconnexion du réseau.<br/> La version de BITS 1,0 est incluse dans Windows XP.<br/> La version de% windir% \System32\QMgr.dll est &quot; 6.0. xxxx. xxxx &quot; .<br/></td>
</tr>
</tbody>
</table>

Pour illuminer les fonctionnalités de votre programme en fonction des fonctionnalités de BITS, utilisez QueryInterface sur (par exemple) votre objet de travail pour voir si l’objet de tâche vous permet de créer la version dont vous avez besoin. Vous pouvez également consulter la rubrique [détermination de la version de bits sur un ordinateur](./determining-the-version-of-bits-on-a-computer.md) pour convertir le numéro de version QMgr.dll en version bits.

## <a name="version-103"></a>Version 10,3

Les interfaces suivantes ont été ajoutées pour cette version
-   [**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3) 
     [ **IBackgroundCopyServerCertificateValidationCallback**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)


## <a name="version-102"></a>Version 10,2

Les interfaces suivantes ont été ajoutées pour cette version
-   [**IBackgroundCopyJobHttpOptions2**](/windows/win32/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2)


## <a name="version-101"></a>Version 10,1

Les interfaces suivantes ont été ajoutées pour cette version
-   [**BackgroundCopyFile6**](/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6)
-   [**IBackgroundCopyCallback3**](/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)

Les constantes suivantes ont été ajoutées pour être utilisées avec l' [énumération BITS_JOB_PROPERTY_ID](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id).

-   **\_propriété de tâche bits en \_ \_ \_ mode de demande \_**
-   **\_intervalle de \_ notification minimal de la propriété du travail bits \_ \_ \_ \_ ms**


## <a name="version-50"></a>Version 5.0

Les interfaces suivantes ont été ajoutées pour cette version :

-   [**IBackgroundCopyJob5**](/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)

## <a name="version-40"></a>Version 4.0

Les interfaces suivantes ont été ajoutées pour cette version :

-   [**IBitsToken**](/windows/win32/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
-   [**IBackgroundCopyFile4**](/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4)

## <a name="version-30"></a>Version 3.0

Les interfaces suivantes ont été ajoutées pour cette version :

-   [**IBackgroundCopyCallback2**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)
-   [**IBackgroundCopyFile3**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3)
-   [**IBackgroundCopyJob4**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)
-   [**IBitsPeer**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeer)
-   [**IBitsPeerCacheAdministration**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration)
-   [**IBitsPeerCacheRecord**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacherecord)
-   [**IEnumBitsPeerCacheRecords**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords)
-   [**IEnumBitsPeers**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeers)

Les constantes suivantes ont été ajoutées pour être utilisées avec la méthode [**IBackgroundCopyJobHttpOptions :: SetSecurityFlags**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) :

-   **\_ \_ la stratégie de redirection http BG \_ autorise le \_ \_ silence**
-   **\_ \_ \_ rapport autoriser la stratégie de REdirection http \_ BG \_**
-   **\_interdiction de \_ la stratégie de redirection http BG \_ \_**
-   **\_masque de \_ stratégie de redirection http \_ BG \_**
-   **\_ \_ la stratégie de redirection http BG \_ \_ autorise \_ https \_ à \_ http**

## <a name="version-25"></a>Version 2.5

L’interface et l’énumération suivantes ont été ajoutées pour la version 2,5 :

-   [**IBackgroundCopyJobHttpOptions**](/windows/win32/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions)
-   [**\_emplacement du \_ magasin de certificats BG \_**](/windows/win32/api/Bits2_5/ne-bits2_5-bg_cert_store_location)

## <a name="version-20"></a>Version 2.0

Les interfaces, la structure et les rubriques suivantes ont été ajoutées pour la version 2,0 :

-   [**IBackgroundCopyJob3**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)
-   [**IBackgroundCopyFile2**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2)
-   [**\_plage de fichiers BG \_**](/windows/win32/api/Bits2_0/ns-bits2_0-bg_file_range)
-   [Stratégies de groupe](group-policies.md)

Pour plus d’informations sur les téléchargements simultanés au premier plan, consultez la section Notes pour la [**\_ \_ priorité du travail BG**](/windows/win32/api/Bits/ne-bits-bg_job_priority).

Pour plus d’informations sur l’utilisation du protocole SMB, consultez [**\_ \_ informations sur le fichier BG**](/windows/win32/api/Bits/ns-bits-bg_file_info).

## <a name="version-15"></a>Version 1.5

Les interfaces et rubriques suivantes ont été ajoutées pour la version 1,5 :

-   [**IBackgroundCopyJob2**](/windows/win32/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
-   [Récupération de la réponse d’un travail de Upload-Reply](retrieving-the-reply-from-an-upload-reply-job.md)
-   [Inscription pour exécuter un programme](registering-to-execute-a-program.md)
-   [Paramètres du serveur BITS pour les travaux de chargement](bits-server-settings-for-upload-jobs.md)
-   [Configuration du serveur pour les téléchargements](setting-up-the-server-for-uploads.md)
-   [Utilisation d’en-têtes de demande/réponse de notification BITS](using-bits-notification-request-response-headers.md)

 
## <a name="updating-bits-versions"></a>Mise à jour des versions BITS
 
Vous pouvez télécharger BITS 4,0 pour Windows Server 2008 avec Service Pack 2 (SP2), Windows Vista avec Service Pack 1 (SP1) et Windows Vista avec Service Pack 2 (SP2). Pour plus d’informations sur le téléchargement de BITS 4,0, consultez [l’article KB968929](https://support.microsoft.com/kb/968929).
