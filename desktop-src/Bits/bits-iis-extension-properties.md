---
title: Propriétés des extensions IIS BITS
description: Service de transfert intelligent en arrière-plan (BITS) utilise une ISAPI pour étendre IIS afin de prendre en charge les travaux de chargement.
ms.assetid: 08a40cc1-ec6d-4b65-971a-15c7b06df148
keywords:
- BITS des propriétés d’extension IIS BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c81d57114a23a07c5f952a9cb33399644f5cbed8bbf67cccf802a1c996b72b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835168"
---
# <a name="bits-iis-extension-properties"></a>Propriétés des extensions IIS BITS

Service de transfert intelligent en arrière-plan (BITS) utilise une ISAPI pour étendre IIS afin de prendre en charge les [**travaux de chargement**](/windows/win32/api/bits/ne-bits-bg_job_type). Le tableau suivant répertorie les propriétés que BITS ajoute à la métabase IIS pour le composant de répertoire virtuel. BITS utilise ces propriétés pour déterminer comment télécharger les fichiers. Les propriétés d’extension IIS BITS peuvent être héritées, à l’exception de **BITSUploadEnabled**.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BITSUploadEnabled</strong> Type de données : <strong>booléen</strong><br/></td>
<td>Indique si les téléchargements BITS sont activés sur le répertoire virtuel. Si le paramètre n’est pas présent ou s’il est égal à 0, les téléchargements BITS sont désactivés.<br/> Il s’agit d’une propriété en lecture seule. Pour définir cette propriété, appelez la méthode <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads"><strong>EnableBITSUploads</strong></a> ou <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-disablebitsuploads"><strong>DisableBITSUploads</strong></a> de l’interface <a href="/windows/win32/api/bitscfg/nn-bitscfg-ibitsextensionsetup"><strong>IBITSExtensionSetup</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><strong>BITSSessionTimeout</strong> Type de données : <strong>DWORD</strong><br/></td>
<td>Nombre de secondes pendant lesquelles la connexion est conservée si aucune progression n’est effectuée lors du chargement du fichier ; la minuterie est réinitialisée lorsque la progression est effectuée. Le service BITS ferme la connexion si le délai d’expiration est atteint et nettoie les données associées à la session.<br/> La définition d’un délai d’expiration de session court peut être un problème pour les travaux de chargement-réponse, car la réponse est téléchargée uniquement lorsque l’utilisateur est connecté et connecté au réseau. Il est possible que la session expire avant le téléchargement de la réponse. dans ce cas, la session est annulée et le fichier de réponse est supprimé.<br/> Notez que le service BITS annule le travail si la valeur de stratégie de groupe <a href="/windows/win32/bits/group-policies">paramètre jobinactivitytimeout</a> (la valeur par défaut est 90 jours) est atteinte, quel que soit ce paramètre.<br/> La valeur par défaut est 1 209 600 (14 jours).<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSMaximumUploadSize</strong> Type de données : <strong>chaîne</strong><br/></td>
<td>Nombre maximal d’octets qui peuvent être téléchargés par travail. Spécifiez le nombre maximal d’octets sous la forme d’une chaîne décimale ; la valeur de chaîne doit être inférieure ou égale à &quot; 1844674407370955 &quot; . Une chaîne vide est identique à la spécification de &quot; 1844674407370955 &quot; .<br/> La valeur par défaut est une chaîne vide.<br/>
<blockquote>
[!Note]<br />
Dans IIS 7, la limite de téléchargement par défaut est de 30 millions octets. La valeur de la propriété <strong>BITSMaximumUploadSize</strong> ne peut pas dépasser la limite d’IIS. Pour plus d’informations sur la modification de la valeur par défaut IIS, consultez <a href="https://support.microsoft.com//kb/942074">KB942074</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSServerNotificationType</strong> Type de données : <strong>DWORD</strong><br/></td>
<td>Spécifie comment envoyer le fichier de téléchargement à l’application serveur. Les valeurs possibles sont les suivantes : 0, 1 et 2.<br/> La valeur 0 signifie que le fichier n’est pas envoyé à l’application serveur. Le service BITS place le fichier de téléchargement dans le répertoire spécifié dans le nom distant (le nom distant spécifié quand vous avez <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-addfile">ajouté le fichier</a> au travail) sans en avertir l’application serveur. Si le fichier existe actuellement dans le répertoire de destination, il est remplacé par le fichier de téléchargement.<br/> La valeur 1 signifie que le service BITS passe l’emplacement du fichier de téléchargement à l’application serveur spécifiée dans la propriété <strong>BITSServerNotificationURL</strong> . L’application serveur traite le fichier et génère un fichier de réponse, si nécessaire. Par défaut, le service BITS supprime les fichiers de chargement et de réponse du serveur après avoir reçu la réponse de l’application serveur. Pour que le service BITS copie le fichier de téléchargement à l’emplacement spécifié par le nom de fichier distant dans le travail, incluez l’en-tête <a href="/windows/win32/bits/notification-protocol-for-server-applications">bits-Copy-file-to-destination</a> dans votre réponse. Si vous n’incluez pas l’en-tête et que vous souhaitez enregistrer les fichiers de téléchargement et de réponse, vous devez copier les fichiers de chargement et de réponse dans un nouvel emplacement avant de répondre.<br/> La valeur 2 signifie que le service BITS passe le fichier de téléchargement dans le corps de la requête à l’application serveur spécifiée dans la propriété <strong>BITSServerNotificationURL</strong> . L’application serveur traite le fichier et transmet la réponse dans le corps de la réponse, si nécessaire.<br/> Pour plus d’informations sur les en-têtes de demande et de réponse, consultez <a href="/windows/win32/bits/notification-protocol-for-server-applications">protocole de notification pour les applications serveur</a>.<br/> L’application serveur doit fournir une réponse dans un délai de cinq minutes. Si l’application serveur ne répond pas dans les cinq minutes, le travail passe à l’état d’erreur temporaire. Lorsque le <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay"><strong>délai</strong></a> entre deux tentatives expire, le serveur bits envoie une autre notification à l’application serveur (l’application serveur doit être écrite pour gérer les notifications dupliquées). <strong>BITS 1,5 :</strong> Le délai d’attente de la notification est de 30 secondes.<br/> <br/> La valeur par défaut est 0.<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSServerNotificationURL</strong> Type de données : <strong>chaîne</strong><br/></td>
<td>Facultatif. Contient l’URL de l’application serveur vers laquelle BITS publie le fichier de téléchargement. Vous devez spécifier une URL si la valeur de la propriété <strong>BITSServerNotificationType</strong> est 1 ou 2. L’URL est limitée à 2 200 caractères, à l’exclusion de la marque de fin null. L’URL doit être une URL HTTP ; BITS ne prend pas en charge les URL de notification HTTPs.<br/> Si l’URL n’est pas disponible au moment du chargement, le service BITS tente à nouveau le téléchargement jusqu’à ce que l’URL de notification existe ou que la période de nouvelle tentative expire.<br/> Notez que si le nom distant spécifié dans le travail contient une chaîne de requête, la chaîne de requête est ajoutée à l’URL que vous spécifiez. Par exemple, si le nom distant contient https://myserver/myvdir/subdir/file.asp?ACCOUNT=86433 et que vous spécifiez le paramètre <strong>BITSServerNotificationURL</strong> comme https://otherserver/myvdir2/bag.asp , l’URL vers laquelle bits est publié est https://otherserver/myvdir2/bag.asp?ACCOUNT=86433 .<br/> Si l’URL d’origine est https://myserver/myvdir/file.txt et que l’URL de notification est myasp. asp, bits utilise http//MyServer/myvdir/myasp. asp comme URL de notification.<br/> Si la partie du chemin d’accès et du nom de fichier de l’URL contient des caractères Unicode qui ne sont pas en commun à la page de codes sur le client et le serveur, la traduction d’URL échoue sur le serveur et le travail BITS est placé dans l’état d’erreur. Si la partie serveur de l’URL contient des caractères Unicode, vous devez encoder la partie serveur à l’aide de <a href="/windows/win32/intl/handling-internationalized-domain-names--idns">noms de domaine internationaux</a> (IDN).<br/></td>
</tr>
<tr class="even">
<td><strong>BITSHostId</strong> Type de données : <strong>chaîne</strong><br/></td>
<td>Définissez cette propriété si l’installation du serveur est une batterie de serveurs Web qui n’utilise pas de stockage partagé.<br/> Spécifiez le nom du serveur ou l’adresse IP du serveur auquel se reconnecter une fois le processus de téléchargement interrompu. En règle générale, vous spécifiez le nom du serveur que vous configurez. L’URL est limitée à 300 caractères, à l’exclusion de la marque de fin null.<br/> Si vous ne spécifiez pas cette propriété et que le processus de téléchargement est interrompu, il est possible que le service BITS reprenne le travail sur un autre serveur de la batterie. Toutefois, le serveur précédent contient toujours le fichier de téléchargement partiel avant l’interruption. BITS supprime le fichier partiel après l’expiration du <strong>BITSSessionTimeout</strong> .<br/>
<blockquote>
[!Note]<br />
N’utilisez pas la propriété <strong>BITSHostId</strong> si le protocole SSL est utilisé dans une batterie de serveurs Web qui utilise l’équilibrage de charge réseau (NLB) ou les noms DNS avec plusieurs adresses IP, sauf si vous incluez le nom du cluster et des noms de serveurs individuels dans le certificat. (Si le nom du serveur spécifié dans <strong>BITSHostId</strong> ne correspond pas au nom commun du certificat, le travail échoue.) Au lieu de cela, pour l’équilibrage de la charge réseau, affectez la valeur <strong>Single</strong> au paramètre <a href="/previous-versions/tn-archive/bb687542(v=technet.10)">Affinity</a> pour vous assurer que le client communique avec le même serveur à l’avenir.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSHostIdFallbackTimeout</strong> Type de données : <strong>DWORD</strong><br/></td>
<td>Nombre de secondes pendant lesquelles le client BITS tente de se reconnecter au nom du serveur <strong>BITSHostId</strong> avant de revenir au nom d’hôte spécifié dans le nom de fichier distant du travail. La minuterie commence lorsque le service BITS ne parvient pas à se connecter au serveur <strong>BITSHostId</strong> . La minuterie est réinitialisée lorsque le client se connecte correctement au serveur.<br/> Notez que la valeur du délai d’attente de non-progression du travail (consultez <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout"><strong>méthode ibackgroundcopyjob :: SetNoProgressTimeout</strong></a>) doit être supérieure à cette valeur de délai d’attente. Si ce n’est pas le cas, le travail échoue avant l’expiration de la valeur du délai d’attente de secours.<br/> Définissez cette propriété uniquement si vous définissez la propriété <strong>BITSHostId</strong> .<br/> La valeur par défaut est 86 400 (1 jour).<br/></td>
</tr>
<tr class="even">
<td><strong>BITSAllowOverwrites</strong> Type de données : <strong>entier</strong><br/></td>
<td>Indique si un fichier de téléchargement peut remplacer un fichier existant portant le même nom. Le fichier de chargement remplace le fichier existant si <strong>BITSAllowOverwrites</strong> est 1.<br/> La valeur par défaut est 0.<br/> <strong>IIS 6,0 :</strong> Vous pouvez définir cette propriété uniquement à partir d’un script, vous ne pouvez pas la définir à l’aide de la page Propriétés de l’extension BITS dans l’interface utilisateur IIS.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUseDefault</strong> Type de données : <strong>booléen</strong><br/></td>
<td>Indique si la tâche de nettoyage utilise les planifications par défaut. Par défaut, la tâche de nettoyage est exécutée toutes les 12 heures.<br/> Définir sur 1 pour utiliser la planification par défaut ; dans le cas contraire, 0 pour spécifier une planification.<br/> Pour spécifier une planification, utilisez les propriétés <strong>BITSCleanupCount</strong> et <strong>BITSCleanupUnits</strong> .<br/> La tâche de nettoyage nettoie le répertoire virtuel en supprimant les travaux qui n’ont pas été modifiés au cours du délai d’attente de la session (voir <strong>BITSSessionTimeout</strong>).<br/> La valeur par défaut est 1 utiliser la planification par défaut.<br/> <strong>IIS 6,0 :</strong> Non pris en charge.<br/></td>
</tr>
<tr class="even">
<td><strong>BITSCleanupCount</strong> Type de données : <strong>entier</strong><br/></td>
<td>Spécifie l’intervalle d’attente entre l’exécution de la tâche de nettoyage. L’intervalle que vous pouvez spécifier dépend des unités. Pour connaître les valeurs d’intervalle possibles, consultez la propriété <strong>BITSCleanupUnits</strong> .<br/> Cette propriété est ignorée si <strong>BITSCleanupUseDefault</strong> est égal à 0.<br/> <strong>IIS 6,0 :</strong> Non pris en charge.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUnits</strong> Type de données : <strong>entier</strong><br/></td>
<td>Spécifie les unités pour l’intervalle de nettoyage spécifié dans la propriété <strong>BITSCleanupCount</strong> . Cette propriété est ignorée si <strong>BITSCleanupUseDefault</strong> est égal à 0.<br/> Les valeurs possibles sont les suivantes :<dl> 0 : les unités sont des minutes. Les valeurs possibles sont comprises entre 1 et 60.<br />
1 : les unités sont des heures. Il s’agit de la valeur par défaut. Les valeurs possibles sont comprises entre 1 et 24.<br />
2 : les unités sont des jours. Les valeurs possibles sont comprises entre 1 et 360.<br />
</dl> <br/> <strong>IIS 6,0 :</strong> Non pris en charge.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSNumberOfSessionsLimit</strong> Type de données : <strong>entier</strong><br/></td>
<td>Limite le nombre de sessions de téléchargement pouvant exister simultanément pour un utilisateur. Si le nombre de sessions d’un utilisateur dépasse cette limite, lorsque la tâche de nettoyage s’exécute, elle supprime les sessions les plus récentes jusqu’à ce que le nombre de sessions pour l’utilisateur soit inférieur à la limite.<br/> La valeur par défaut est 50 sessions.<br/> <strong>IIS 6,0 :</strong> Non pris en charge.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSSessionLimitEnable</strong> Type de données : <strong>booléen</strong><br/></td>
<td>Indique si BITS limite le nombre de sessions de téléchargement par utilisateur. Si le paramètre n’est pas présent ou s’il est égal à 0, la limite est désactivée.<br/> Pour spécifier la limite, définissez la propriété <strong>BITSNumberOfSessionsLimit</strong> .<br/> La valeur par défaut est 1.<br/> <strong>IIS 6,0 :</strong> Non pris en charge.<br/> <br/></td>
</tr>
</tbody>
</table>



 

l’exemple suivant montre comment définir les propriétés d’extension IIS BITS à l’aide d’Windows Script Host. Si le répertoire virtuel pointe vers un partage distant, définissez également les propriétés IIS **UNCUserName** et **UNCPassword** .


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

// Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



 

