---
description: La propriété transformations est une liste des transformations appliquées par le programme d’installation lors de l’installation du package.
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: Transformations (propriété)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f873e439ef9542efa618a8e86c9667a3c962939f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474315"
---
# <a name="transforms-property"></a>Transformations (propriété)

La propriété **TRANSformations** est une liste des transformations appliquées par le programme d’installation lors de l’installation du package. Le programme d’installation applique les transformations dans le même ordre que celui dans lequel elles sont répertoriées dans la propriété. Les transformations peuvent être spécifiées par leur nom de fichier ou leur chemin d’accès complet. Pour spécifier plusieurs transformations, séparez chaque nom de fichier ou chemin d’accès complet par un point-virgule (;). Par exemple, pour appliquer trois transformations à un package, définissez **TRANSformations** sur une liste de noms de fichiers ou sur une liste de chemins d’accès complets.

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

Vous pouvez indiquer qu’un fichier de transformation est incorporé dans un stockage du fichier .msi, plutôt qu’en tant que fichier autonome, en préfixant le nom de fichier avec un signe deux-points ( :). Par exemple, l’exemple suivant indique que transform1. MST et transform2. MST sont incorporés dans le fichier .msi et que transform3. MST est un fichier autonome.

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

Le programme d’installation requiert les transformations figurant dans les **TRANSformations** à chaque installation, publication, installation à la demande ou installation de maintenance du package. La stratégie de [stratégie TransformsSecure](transformssecure-policy.md) , la propriété **transformations** et le premier caractère de la chaîne **transformations** informe le programme d’installation de la gestion de la résilience source des fichiers de transformation autonomes. Windows Le programme d’installation traite la définition de la [stratégie TransformsAtSource](transformsatsource-policy.md) ou [**TransformsAtSource**](transformsatsource.md) la même chose que la stratégie TransformsSecure et [**TransformsSecure**](transformssecure.md). Notez que les transformations incorporées dans le fichier .msi ne sont pas mises en cache et sont toujours obtenues à partir du package.




| Transformations (propriété) | Transformations sécurisées | Mise en cache et résilience | 
|---------------------|-------------------|------------------------|
| @ [<em>liste des noms de</em>fichiers] exemple :<br /> @transform1.mst; transform2. MST ; transform3. MST<br /> | Aucun effet. | <a href="secure-at-source-transforms.md">Transformations sécurisées au niveau de la source</a>. La source des transformations doit se trouver à la racine de la source du package. Lorsque le package est installé ou publié, le programme d’installation enregistre les transformations sur l’ordinateur de l’utilisateur dans un cache où l’utilisateur ne dispose pas d’un accès en écriture. Si la copie locale de la transformation devient indisponible, le programme d’installation recherche une source pour restaurer le cache. La méthode est identique à la recherche d’un fichier .msi dans la liste source. Consultez <a href="source-resiliency.md">résilience source</a>. | 
| |[<em>liste des chemins d’accès</em>] Tels<br /><pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.MST ; \\ server2\share2\path2\transform2.mst</code></pre> | Aucun effet. | <a href="secure-full-path-transforms.md">Les transformations sécurisées-chemin d’accès complet</a>. La source de chaque transformation doit être au chemin d’accès complet passé aux <strong>TRANSformations</strong>. La source de la transformation ne doit pas être située à la source du package. Lorsque le package est installé ou publié, le programme d’installation enregistre les transformations sur l’ordinateur de l’utilisateur dans un cache où l’utilisateur ne dispose pas d’un accès en écriture. Si la copie locale de la transformation devient indisponible, le programme d’installation peut uniquement restaurer le cache à partir de la source au chemin d’accès spécifié. | 
| [<em>liste des noms de</em>fichiers] Le premier caractère n’est pas @ ou |.<br /> Exemple :<br /> transform1. MST ; transform2. MST ; transform3. MST<br /> | <a href="transformssecure-policy.md">TransformsSecure stratégie</a> ou <a href="transformssecure.md"><strong>TransformsSecure</strong></a> défini sur 1 ou<br />La <a href="transformsatsource-policy.md">stratégie TransformsAtSource</a> ou <a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> a la valeur 1.<br /> | Si <strong>TRANSformations</strong> est une liste de noms de fichiers, le programme d’installation les traite comme des <a href="secure-at-source-transforms.md">transformations sécurisées au niveau</a>de la source. Si <strong>TRANSformations</strong> est une liste de chemins d’accès complets, le programme d’installation les traite comme des <a href="secure-full-path-transforms.md">transformations sécurisées de chemin d’accès complet</a>.<br /> | 
| [<em>liste des noms de</em>fichiers] Le premier caractère n’est pas @ ou |.<br /> Exemple :<br /> transform1. MST ; transform2. MST ; transform3. MST<br /> | La <a href="transformssecure-policy.md">stratégie TransformsSecure</a> et <a href="transformssecure.md"><strong>TransformsSecure</strong></a> ne sont pas définis et<br />La <a href="transformsatsource-policy.md">stratégie TransformsAtSource</a> et <a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> ne sont pas définis.<br /> | <a href="unsecured-transforms.md">Transformations non sécurisées</a>. La source des transformations doit se trouver à la racine de la source du package. Lorsque le package est installé ou publié par utilisateur, le programme d’installation enregistre les transformations dans le profil de l’utilisateur. Cela permet à un utilisateur de se déplacer entre les ordinateurs tout en conservant leurs personnalisations. Pour une installation par ordinateur, la transformation est enregistrée dans le dossier%windir%\Installer. Si la copie locale de la transformation devient indisponible, le programme d’installation recherche une source pour restaurer le cache. La méthode est identique à la recherche d’un fichier .msi dans la liste source. Consultez <a href="source-resiliency.md">résilience source</a>. | 
| [<em>liste des chemins d’accès</em>] Le premier caractère n’est pas @ ou |.<br /> Exemple :<br /><pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre> | La <a href="transformsatsource-policy.md">stratégie TransformsAtSource</a> et <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> ne sont pas définis et<br />La <a href="transformsatsource-policy.md">stratégie TransformsAtSource</a> et <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> ne sont pas définis.<br /> | <a href="unsecured-transforms.md">Transformations non sécurisées</a>. Lorsque le package est installé ou publié par utilisateur, le programme d’installation enregistre les transformations dans le profil de l’utilisateur. Cela permet à un utilisateur de se déplacer entre les ordinateurs tout en conservant leurs personnalisations. Pour une installation par ordinateur, la transformation est enregistrée dans le dossier%windir%\Installer. Si la copie locale de la transformation devient indisponible, le programme d’installation recherche une source pour restaurer le cache. La méthode est identique à la recherche d’un fichier .msi dans la liste source. Consultez <a href="source-resiliency.md">résilience source</a>. | 




 

Vous ne pouvez pas utiliser les noms de fichiers et les chemins d’accès dans la même liste **TRANSformations** . Vous ne pouvez pas spécifier des transformations sécurisées et de profil ensemble dans la même liste. Vous pouvez inclure des transformations incorporées dans le package dans une liste avec d’autres transformations.

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

Notez que, étant donné que le séparateur de liste des transformations est le point-virgule, les points-virgules ne doivent pas être utilisés dans un nom de fichier ou un chemin d’accès de transformation.

## <a name="remarks"></a>Remarques

dans les cas où la propriété [TransformsSecure](transformssecure-policy.md) ou [**TransformsSecure**](transformssecure.md) a été définie avec Windows Installer, il n’est pas nécessaire de passer le symbole @ ou \| lors de la définition des **transformations** à l’aide de la ligne de commande. Le programme d’installation suppose qu’il s’agit d’un chemin sécurisé à source ou sécurisé-complet si la liste se compose uniquement de noms de fichiers situés à la source ou se compose uniquement de chemins d’accès complets. Vous ne pouvez toujours pas mélanger les deux types de sources de transformation.

Notez que le programme d’installation utilise un ordre de recherche différent pour les transformations non sécurisées appliquées lors de la première installation et de la maintenance. Pour plus d’informations, consultez [transformations non sécurisées](unsecured-transforms.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Transformations de base de données](database-transforms.md)
</dt> <dt>

[Fusions et transformations](merges-and-transforms.md)
</dt> <dt>

[Résilience source](source-resiliency.md)
</dt> </dl>

 

 




