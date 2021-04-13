---
description: Lorsque vous développez votre propre application VSS, vous devez respecter les instructions et restrictions suivantes.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilité des applications VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318409"
---
# <a name="vss-application-compatibility"></a>Compatibilité des applications VSS

Lorsque vous développez votre propre application VSS, vous devez respecter les instructions et restrictions suivantes. Il peut s’avérer utile de faire référence à l’exemple de code pour les demandeurs VSS, les fournisseurs et les rédacteurs fournis dans le kit de développement logiciel (SDK) Microsoft Windows.

> [!Note]  
> Le SDK Windows peut être utilisé pour développer des applications VSS uniquement pour Windows Vista et les versions ultérieures du système d’exploitation Windows. Elle ne peut pas être utilisée pour développer des demandeurs VSS, des fournisseurs ou des enregistreurs pour Windows Server 2003 R2, Windows Server 2003 ou Windows XP.

 

**Windows server 2003 R2, Windows server 2003 et Windows XP :** VSS est disponible dans le kit de développement logiciel (SDK) Service VSS 7,2, que vous pouvez télécharger à partir de [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) . Notez que les fichiers vssapi. lib 64 bits dans les répertoires du répertoire Win2003 \\ obj peuvent être utilisés pour les versions 64 bits de Windows server 2003 R2, Windows server 2003 et Windows XP. Ce kit de développement logiciel (SDK) fournit également un exemple de code pour les demandeurs VSS, les fournisseurs et les writers.

## <a name="compiling-vss-applications"></a>Compilation d’applications VSS

Lors du développement d’un demandeur, par exemple une application de sauvegarde :

-   Incluez les en-têtes suivants : <dl> VSS. h  
    VsWriter. h  
    VsBackup. h  
    </dl>
-   Link the following library: <dl> VssApi. lib  
    </dl>

Lors du développement d’un enregistreur :

-   Incluez les en-têtes suivants : <dl> VSS. h  
    VsWriter. h  
    </dl>
-   Link the following library: <dl> VssApi. lib  
    </dl>

## <a name="supported-configurations-and-restrictions"></a>Configurations et restrictions prises en charge

La liste suivante décrit les configurations et restrictions prises en charge :

-   VSS est fourni et pris en charge sur les versions du système d’exploitation Windows à compter de Windows XP.
-   Le tableau suivant récapitule les informations de compatibilité entre les différentes versions de Windows. Notez que si une application VSS est « compilée pour » une version de Windows spécifiée, cela signifie que l’application a été compilée à l’aide des fichiers d’en-tête et des bibliothèques qui sont spécifiques à cette version.

    > [!Note]  
    > Les fournisseurs de matériel s’exécutent uniquement sur les versions de système d’exploitation Windows Server. Ils ne s’exécuteront pas sur les versions des systèmes d’exploitation clients Windows.

     

    > [!Note]  
    > Dans les tableaux suivants, Windows Server 2008 avec Service Pack 2 (SP2) doit être considéré comme le même que Windows Server 2008. Pour plus d’informations sur Windows Server 2008 avec SP2, consultez <https://go.microsoft.com/fwlink/p/?linkid=178730> . Windows Server 2003 R2 doit être considéré comme Windows Server 2003.

     

    > [!Note]  
    > Si une application VSS est compilée pour Windows Server 2003 ou une version ultérieure, elle s’exécutera également sur les versions ultérieures de Windows.

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Redemandeurs VSS, enregistreurs et fournisseurs compilés pour</th>
    <th>S’exécutera sur</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) et Windows Vista (64 bits)</td>
    <td>Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) et Windows Vista (64 bits)</td>
    </tr>
    <tr class="even">
    <td>Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) et Windows Vista (32 bits)</td>
    <td>Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) et Windows Vista (32 bits)</td>
    </tr>
    <tr class="odd">
    <td>Windows Server 2003 (64 bits)</td>
    <td>Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits), Windows Vista (64 bits) et Windows Server 2003 (64 bits)</td>
    </tr>
    <tr class="even">
    <td>Windows Server 2003 (32 bits)</td>
    <td>Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits), Windows Vista (32 bits) et Windows Server 2003 (32 bits) <blockquote>
    [!Note]<br />
Les demandeurs s’exécuteront également sur Windows Server 2003 (64 bits).
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>Windows XP Édition 64 bits</td>
    <td>Windows Server 2003 (64 bits) et Windows XP 64 bits Edition</td>
    </tr>
    <tr class="even">
    <td>Windows XP (32 bits)</td>
    <td>Windows XP (32 bits)</td>
    </tr>
    </tbody>
    </table>

    

     

    

    | Pour compiler un demandeur, un enregistreur ou un fournisseur VSS pour        | Utilisation                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows Server 2008 R2 ou Windows 7                        | SDK Windows pour Windows 7 (disponible à partir du [Centre de téléchargement Windows](https://www.microsoft.com/download/details.aspx?id=8279)).                |
    | Windows Server 2008 ou Windows Vista                       | SDK Windows pour Windows Server 2008 (disponible dans le [Centre de développement SDK Windows](https://msdn.microsoft.com/windows/bb980924.aspx).) |
    | Windows Server 2003 R2, Windows Server 2003 ou Windows XP | [Kit de développement logiciel (SDK) Service VSS 7,2](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   Toutes les applications VSS 32 bits (demandeurs, fournisseurs et enregistreurs) doivent s’exécuter en tant qu’applications natives 32 bits ou 64 bits. Leur exécution sous WOW64 n’est pas prise en charge.

    **Windows Server 2003 et Windows XP :** L’exécution de demandeurs VSS 32 bits sous WOW64 est prise en charge, mais pas pour les sauvegardes de l’état du système. L’exécution des fournisseurs et des enregistreurs VSS 32 bits sous WOW64 n’est pas prise en charge. La prise en charge de l’exécution de demandeurs 32 bits sous WOW64 a été supprimée dans Windows Vista et les versions ultérieures.

-   Un cliché instantané créé sur Windows Server 2003 R2 ou Windows Server 2003 ne peut pas être utilisé sur un ordinateur qui exécute Windows Server 2008 R2 ou Windows Server 2008. Un cliché instantané créé sur Windows Server 2008 R2 ou Windows Server 2008 ne peut pas être utilisé sur un ordinateur qui exécute Windows Server 2003. Toutefois, un cliché instantané créé sur Windows Server 2008 peut être utilisé sur un ordinateur qui exécute Windows Server 2008 R2, et vice versa.
-   Pour prendre en charge les clichés instantanés, un système exécutant VSS doit avoir au moins un système de fichiers NTFS. Ce système de fichiers hébergera la « zone diff » du cliché instantané. Pour plus d’informations, consultez [fournisseur système](providers.md).
-   Compte tenu de la présence d’un système de fichiers NTFS et du choix approprié du contexte (consultez [configurations du contexte](shadow-copy-context-configurations.md)de cliché instantané), tous les systèmes de fichiers locaux pris en charge peuvent être des clichés instantanés.
-   Vous pouvez créer des clichés instantanés uniquement pour les systèmes de fichiers montés localement. Les partages distants et autres systèmes de fichiers montés sur plusieurs systèmes de fichiers ne peuvent pas être des clichés instantanés par le système qui les monte. Ces systèmes de fichiers peuvent être des clichés instantanés uniquement par les systèmes qui traitent les systèmes de fichiers.
-   Les rédacteurs et les demandeurs doivent spécifier uniquement des ressources locales. Les ressources locales sont des ensembles de fichiers dont le chemin d’accès absolu commence par une lettre de lecteur, et la lettre de lecteur ne peut pas être associée à un dossier monté sur un partage distant.
-   Le nombre maximal de clichés instantanés logiciels pour chaque volume est de 512. Toutefois, par défaut, vous ne pouvez conserver que 64 clichés instantanés utilisés par la fonctionnalité Clichés instantanés de dossiers partagés. Pour modifier la limite de la fonctionnalité clichés instantanés de dossiers partagés, utilisez la clé de Registre [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) .
-   L’infrastructure des composants de sauvegarde ne prend pas en charge la sauvegarde des ressources de cluster en tant que composants d’écriture. Pour sauvegarder des ressources de cluster, les applications doivent supposer que le chemin d’accès est local à un nœud de cluster particulier spécifié.
-   [!Note]  
    > Microsoft ne fournit pas de support technique pour les développeurs ou les professionnels de l’informatique pour l’implémentation de restaurations en ligne sur l’état du système sur Windows (toutes les versions).

     

    Lors de la sauvegarde et de la récupération de l’état du système, la stratégie recommandée consiste à sauvegarder et à récupérer les volumes système et de démarrage en plus des fichiers énumérés par les Writers d’État du système.

    > [!Note]  
    > Les Writers d’État du système sont des enregistreurs dont l’attribut de [**\_ \_ type d’utilisation VSS**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) est défini sur VSS \_ ut \_ BOOTABLESYSTEMSTATE ou VSS \_ ut \_ SYSTEMSERVICE.

     

 

 
