---
description: Le compilateur format MOF (MOF) analyse un fichier contenant des instructions MOF et ajoute les classes et les instances de classe définies dans le fichier à l’espace de stockage WMI.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: mofcomp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010449"
---
# <a name="mofcomp"></a>mofcomp

Le compilateur [*format MOF (MOF)*](gloss-m.md) analyse un fichier contenant des instructions MOF et ajoute les classes et les instances de classe définies dans le fichier à l’espace de stockage WMI. Les fichiers MOF sont généralement compilés automatiquement lors de l’installation des systèmes avec lesquels ils sont fournis, mais vous pouvez également compiler les fichiers MOF à l’aide de cet outil.

Pour plus d’informations sur la localisation et l’utilisation de mofcomp.exe, consultez [utilisation des outils de gestion WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)). Pour plus d’informations sur la suppression de classes et d’instances de l’espace de stockage WMI, consultez la commande de préprocesseur [**pragma deleteclass**](pragma-deleteclass.md) .

L’exemple de code suivant montre comment exécuter le compilateur MOF sur un fichier.

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a>Commutateurs

<dl> <dt>

<span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-récupération automatique**
</dt> <dd>

Ajoute le fichier MOF nommé à la liste des fichiers compilés au cours de la récupération du référentiel. La liste des fichiers MOF de récupération automatique est stockée dans la clé de Registre :

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**

Les fichiers MOF listés dans cette entrée de Registre doivent résider sur l’ordinateur local, car les fichiers MOF qui utilisent la commande **AutoRecover** ne peuvent pas récupérer les fichiers MOF situés sur un ordinateur distant.

> [!Note]  
> Pour vous assurer que toutes les définitions de classe WMI pour les objets managés sont restaurées dans l' [*espace de stockage WMI*](gloss-w.md) en cas d’échec et de redémarrage de WMI, utilisez l’instruction [**\# pragma AutoRecover**](pragma-autorecover.md) de préprocesseur dans votre fichier [*format MOF*](gloss-m.md) (MOF).

 

</dd> <dt>

<span id="-check"></span><span id="-CHECK"></span>**-vérifier**
</dt> <dd>

Demande que le compilateur effectue une vérification de la syntaxe uniquement et imprime les messages d’erreur appropriés. Aucun autre commutateur ne peut être utilisé avec ce commutateur. lorsque ce commutateur est utilisé, aucune connexion à Windows Management Instrumentation (WMI) n’est établie et aucune modification n’est apportée au référentiel wmi.

</dd> <dt>

<span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N : <** _NamespacePath_*_>_*
</dt> <dd>Demande que le compilateur charge le fichier MOF dans l’espace de noms spécifié en tant que *NamespacePath*. Le MOF compilé est chargé dans l’espace de noms mofcomp par défaut, racine \\ par défaut, sauf si ce commutateur est utilisé. Vous pouvez également insérer l’espace de noms du pragma de commande du préprocesseur **\# («**_chemin d’accès de l’espace de noms_*_»)_* dans le fichier MOF pour obtenir le même effet. Si le commutateur **-N :** et la commande de l' \# <a href="pragma-namespace.md">espace de noms pragma</a> sont utilisés, la \# **récupération automatique** de l' **espace de noms pragma** est prioritaire. Dans ce cas, la seule façon de compiler le MOF dans un autre espace de noms consiste à modifier le fichier MOF et à modifier la \# commande **pragma namespace** . Un ordinateur distant peut être spécifié à l’aide de la \\ \\ \\ racine MachineName \\ default.</dd> <dt>

<span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-Class : CreateOnly**
</dt> <dd>

Demande que le compilateur n’apporte aucune modification aux classes existantes. Lorsque ce commutateur est utilisé, l’opération de compilation se termine si une classe spécifiée dans le fichier MOF existe déjà.

</dd> <dt>

<span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-Class : ForceUpdate**
</dt> <dd>

Force les mises à jour des classes lorsque des classes enfants sont en conflit. Par exemple, supposons qu’un qualificateur de classe est défini dans une classe enfant et que la classe de base tente d’ajouter le même qualificateur. Dans la **classe :** le mode ForceUpdate, le compilateur MOF résout ce conflit en supprimant le qualificateur en conflit dans la classe enfant. Si la classe enfant a des instances, la mise à jour forcée échoue.

</dd> <dt>

<span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-Class : safeupdate**
</dt> <dd>

Autorise les mises à jour des classes, même s’il existe des classes enfants, à condition que la modification n’entraîne pas de conflits avec les classes enfants. Par exemple, cet indicateur permet d’ajouter une nouvelle propriété à la classe de base qui n’a pas été mentionnée précédemment dans les classes enfants. Si les classes enfants ont des instances, la mise à jour échoue.

</dd> <dt>

<span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-Class : updateonly**
</dt> <dd>

Demande que le compilateur ne crée pas de nouvelles classes. Lorsque ce commutateur est utilisé, l’opération de compilation se termine si une classe spécifiée dans le fichier MOF n’existe pas.

</dd> <dt>

<span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance : updateonly**
</dt> <dd>

Demande que le compilateur ne crée pas de nouvelles instances. Lorsque ce commutateur est utilisé, l’opération de compilation se termine si une instance spécifiée dans le fichier MOF n’existe pas.

</dd> <dt>

<span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance : CreateOnly**
</dt> <dd>

Demande que le compilateur n’apporte aucune modification aux instances existantes. Lorsque ce commutateur est utilisé, l’opération de compilation se termine si une instance spécifiée dans le fichier MOF existe déjà.

</dd> <dt>

<span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B : <** _nom de fichier_*_>_*
</dt> <dd>

Demande que le compilateur crée une version binaire du fichier MOF portant le nom *filename* sans apporter de modification au référentiel WMI.

Si vous utilisez l’option **-B : <** _nom_ *_>_* de fichier pour créer un fichier MOF binaire, seules les versions de qualificateur par défaut sont stockées dans le référentiel WMI.

Le format MOF binaire est le format intermédiaire pour combiner un pilote WDM avec le MOF en tant que ressource. Le MOF binaire représente des classes et des instances comme un fichier MOF de texte et est compressé avant d’être stocké sur le disque.

</dd> <dt>

<span id="-WMI"></span><span id="-wmi"></span>**-WMI**
</dt> <dd>

Demande que le compilateur effectue une vérification de la syntaxe WMI. Le commutateur **-B :** doit être utilisé avec ce commutateur. Le commutateur **-WMI** est utilisé uniquement pour générer des fichiers MOF binaires utilisables par les pilotes de périphériques WDM. Ce commutateur appelle un vérificateur de fichiers MOF binaire distinct qui s’exécute après la création du fichier MOF binaire.

</dd> <dt>

<span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P : <** _mot de passe_*_>_*
</dt> <dd>

*Spécifie le mot de* passe pour l’utilisateur de l’ordinateur à entrer lors de la connexion.

</dd> <dt>

<span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U : <** _nom d’utilisateur_*_>_*
</dt> <dd>

Spécifie le nom d’utilisateur comme nom de l' *utilisateur qui ouvre* une session.

</dd> <dt>

<span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A :** _autorité_ <*_>_*
</dt> <dd>

Spécifie l' *autorité* en tant qu’autorité (nom de domaine) à utiliser lors de la connexion à WMI.

</dd> <dt>

<span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF :** _chemin d’accès_ <*_>_*
</dt> <dd>

Nom de la sortie neutre de la langue. Utilisé avec le commutateur **-Amendement** pour spécifier le nom du fichier MOF indépendant de la langue qui sera généré.

</dd> <dt>

<span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL :** _chemin d’accès_ <*_>_*
</dt> <dd>

Nom de la sortie spécifique à la langue. Utilisé avec le commutateur **-Amendement** pour spécifier le nom du fichier MOF propre à la langue qui sera généré.

</dd> <dt>

<span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-Amendement : <** _paramètres régionaux_*_>_*
</dt> <dd>

Divise le fichier MOF en versions indépendantes du langage et spécifiques. Le compilateur MOF crée une forme indépendante du langage du fichier MOF dont tous les qualificateurs modifiés ont été supprimés. Une version localisée du fichier MOF est également créée avec une extension de nom de fichier MFL. Les paramètres *régionaux* spécifient le nom de l’espace de noms enfant qui contient les définitions de classe localisées. le format des paramètres *régionaux* est MS \_ xxx, où xxx est la valeur hexadécimale de l’Windows LCID. Par exemple, les paramètres régionaux pour l’anglais américain sont MS \_ 409.

</dd> <dt>

<span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <** _resourceName_*_>_*
</dt> <dd>

Extrait le fichier MOF binaire à partir d’une ressource nommée. Ce commutateur obtient le fichier MOF binaire de la classe dans l’espace de stockage WMI, tandis que le commutateur-B crée le format MOF binaire à partir d’un fichier MOF.

</dd> <dt>

<span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L : <** _ResourceLocale_*_>_*
</dt> <dd>

Optionnel. Extrait les descriptions localisées de MOF à partir du fichier MOF binaire en cas d’utilisation avec le commutateur-ER.

</dd> <dt>

<span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*
</dt> <dd>

Nom du fichier à analyser.

</dd> </dl>

## <a name="return-values"></a>Valeurs de retour

Comme première opération, le compilateur MOF effectue une vérification de la syntaxe du fichier MOF. Si le compilateur détecte des erreurs, il affiche un message d’erreur et le processus se termine.

Le compilateur MOF peut retourner les valeurs suivantes :

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

L’opération de compilation MOF a réussi.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Le compilateur MOF n’a pas pu se connecter au serveur WMI. Cela est dû à une erreur sémantique, telle qu’une incompatibilité avec le référentiel WMI existant ou à une erreur réelle, telle que l’échec du démarrage du serveur WMI.

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Un ou plusieurs commutateurs de ligne de commande ne sont pas valides.

</dd> <dt>

<span id="3"></span>1,3
</dt> <dd>

Une erreur de syntaxe MOF s’est produite.

</dd> </dl>

Si le fichier MOF est correctement analysé, mais qu’une tentative est effectuée pour effectuer une opération qui est interdite par un commutateur de ligne de commande, le compilateur retourne un code d’erreur généré par WMI au lieu de l’un des codes de retour répertoriés dans la liste précédente. Par exemple, un code d’erreur WMI est retourné lorsque le commutateur **-instance : updateonly** est spécifié et que le fichier MOF tente de créer une instance.

Si l’instruction de préprocesseur [**\# pragma autoautorecover**](pragma-autorecover.md) ne figure pas dans le fichier, l’avertissement suivant est retourné :

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a>Notes

Le compilateur MOF est disponible dans le répertoire% windir% \\ system32 \\ WBEM. Vous devez spécifier le fichier MOF comme paramètre du compilateur MOF. Vous pouvez également spécifier un commutateur de récupération automatique si vous souhaitez que le fichier MOF soit recompilé automatiquement si le référentiel CIM doit être automatiquement récupéré. Pour plus d’informations, tapez **mofcomp/ ?** à l'invite de commandes.

Un fichier MOF qui utilise le jeu de caractères Unicode contient une signature en tant que deux premiers octets du fichier. Cette signature est U + FFFE ou U + FEFF, en fonction de l’ordre des octets du fichier.

Si aucune erreur ne se produit dans le processus d’analyse, le compilateur MOF se connecte au serveur WMI qui s’exécute sur l’ordinateur local, sauf si le commutateur **-Check** est spécifié. Les classes et les instances définies dans le fichier MOF sont ajoutées à l’espace de stockage WMI.

Lorsqu’une erreur se produit lors de la mise à jour de l’espace de stockage WMI, le compilateur n’effectue aucune tentative pour retourner le référentiel à son état avant le début du traitement du compilateur.

**Windows 8 :** Lors de l’installation d’un fournisseur, mofcomp traite les \[ \] qualificateurs de clé et \[ statique \] comme true s’ils sont présents, indépendamment de leurs valeurs réelles. D’autres qualificateurs sont considérés comme false s’ils sont présents, mais ne sont pas explicitement définis sur true.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**espace de noms pragma**](pragma-namespace.md)
</dt> <dt>

[Compilation des fichiers MOF](compiling-mof-files.md)
</dt> <dt>

[Compilation des fichiers MOF localisés](compiling-localized-mof-files.md)
</dt> <dt>

[Inscription d’un fournisseur](registering-a-provider.md)
</dt> <dt>

[**IMOFCompiler::CompileFile**](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

