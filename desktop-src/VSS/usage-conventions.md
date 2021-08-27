---
description: Lorsque vous développez votre propre application VSS, vous devez respecter les instructions et restrictions suivantes.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilité des applications VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca1f6f3013856087e70247aed21d8f35aa4cf09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483015"
---
# <a name="vss-application-compatibility"></a>Compatibilité des applications VSS

Lorsque vous développez votre propre application VSS, vous devez respecter les instructions et restrictions suivantes. il peut s’avérer utile de faire référence à l’exemple de code pour les demandeurs VSS, les fournisseurs et les rédacteurs fournis dans le kit de développement logiciel (SDK) de Microsoft Windows.

> [!Note]  
> le SDK Windows peut être utilisé pour développer des applications VSS uniquement pour Windows Vista et versions ultérieures Windows les versions de système d’exploitation. il ne peut pas être utilisé pour développer des demandeurs VSS, des fournisseurs ou des enregistreurs pour Windows server 2003 R2, Windows server 2003 ou Windows XP.

 

**Windows server 2003 R2, Windows server 2003 et Windows XP :** VSS est disponible dans le kit de développement logiciel (SDK) Service VSS 7,2, que vous pouvez télécharger à partir de [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) . notez que les fichiers vssapi. lib 64 bits dans les répertoires sous le \\ répertoire Win2003 Obj peuvent être utilisés pour les versions 64 bits de Windows server 2003 R2, Windows server 2003 et Windows XP. Ce kit de développement logiciel (SDK) fournit également un exemple de code pour les demandeurs VSS, les fournisseurs et les writers.

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

-   VSS est fourni et pris en charge sur les versions du système d’exploitation Windows à partir de Windows XP.
-   le tableau suivant récapitule les informations de compatibilité entre les versions de Windows. notez que si une application VSS est « compilée pour » une version de Windows spécifiée, cela signifie que l’application a été compilée à l’aide des fichiers d’en-tête et des bibliothèques qui sont spécifiques à cette version.

    > [!Note]  
    > les fournisseurs de matériel s’exécutent uniquement sur les versions de système d’exploitation Windows server. ils ne s’exécuteront pas sur les versions de système d’exploitation du client Windows.

     

    > [!Note]  
    > dans les tableaux suivants, Windows server 2008 avec Service Pack 2 (SP2) doit être considéré comme Windows server 2008. pour plus d’informations sur Windows Server 2008 avec SP2, consultez <https://go.microsoft.com/fwlink/p/?linkid=178730> . Windows le serveur 2003 R2 doit être considéré comme le même que Windows server 2003.

     

    > [!Note]  
    > si une application VSS est compilée pour Windows Server 2003 ou version ultérieure, elle s’exécutera également sur les versions ultérieures de Windows.

     

    

    
| Redemandeurs VSS, enregistreurs et fournisseurs compilés pour | S’exécutera sur | 
|-----------------------------------------------------|-------------|
| Windows server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) et Windows Vista (64 bits) | Windows server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) et Windows Vista (64 bits) | 
| Windows server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) et Windows Vista (32 bits) | Windows server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) et Windows Vista (32 bits) | 
| Windows Server 2003 (64 bits) | Windows server 2008 R2 (64 bits), Windows 7 (64 bits), Windows server 2008 (64 bits), Windows Vista (64-bit) et Windows Server 2003 (64 bits) | 
| Windows Server 2003 (32 bits) | Windows server 2008 R2 (32 bits), Windows 7 (32 bits), Windows server 2008 (32 bits), Windows Vista (32-bit) et Windows Server 2003 (32 bits)    <blockquote>    [!Note]<br />    les demandeurs s’exécuteront également sur Windows Server 2003 (64 bits).    </blockquote><br /> | 
| Windows XP Édition 64 bits | Windows Server 2003 (64 bits) et Windows XP édition 64 bits | 
| Windows XP (32 bits) | Windows XP (32 bits) | 


    

     

    

    | Pour compiler un demandeur, un enregistreur ou un fournisseur VSS pour        | Utilisation                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows serveur 2008 R2 ou Windows 7                        | Windows kit de développement logiciel (SDK) pour Windows 7 (disponible à partir du [centre de téléchargement Windows](https://www.microsoft.com/download/details.aspx?id=8279).)                |
    | Windows serveur 2008 ou Windows Vista                       | Windows kit de développement logiciel (SDK) pour Windows Server 2008 (disponible dans le [centre de développement SDK Windows](https://msdn.microsoft.com/windows/bb980924.aspx).) |
    | Windows server 2003 R2, Windows server 2003 ou Windows XP | [Kit de développement logiciel (SDK) Service VSS 7,2](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   Toutes les applications VSS 32 bits (demandeurs, fournisseurs et enregistreurs) doivent s’exécuter en tant qu’applications natives 32 bits ou 64 bits. Leur exécution sous WOW64 n’est pas prise en charge.

    **Windows Server 2003 et Windows XP :** L’exécution de demandeurs VSS 32 bits sous WOW64 est prise en charge, mais pas pour les sauvegardes de l’état du système. L’exécution des fournisseurs et des enregistreurs VSS 32 bits sous WOW64 n’est pas prise en charge. la prise en charge de l’exécution de demandeurs 32 bits sous WOW64 a été supprimée dans Windows Vista et les versions ultérieures.

-   un cliché instantané créé sur Windows server 2003 r2 ou Windows server 2003 ne peut pas être utilisé sur un ordinateur exécutant Windows server 2008 r2 ou Windows server 2008. un cliché instantané créé sur Windows server 2008 R2 ou Windows server 2008 ne peut pas être utilisé sur un ordinateur exécutant Windows server 2003. toutefois, un cliché instantané créé sur Windows server 2008 peut être utilisé sur un ordinateur exécutant Windows server 2008 R2, et vice versa.
-   Pour prendre en charge les clichés instantanés, un système exécutant VSS doit avoir au moins un système de fichiers NTFS. Ce système de fichiers hébergera la « zone diff » du cliché instantané. Pour plus d’informations, consultez [fournisseur système](providers.md).
-   Compte tenu de la présence d’un système de fichiers NTFS et du choix approprié du contexte (consultez [configurations du contexte](shadow-copy-context-configurations.md)de cliché instantané), tous les systèmes de fichiers locaux pris en charge peuvent être des clichés instantanés.
-   Vous pouvez créer des clichés instantanés uniquement pour les systèmes de fichiers montés localement. Les partages distants et autres systèmes de fichiers montés sur plusieurs systèmes de fichiers ne peuvent pas être des clichés instantanés par le système qui les monte. Ces systèmes de fichiers peuvent être des clichés instantanés uniquement par les systèmes qui traitent les systèmes de fichiers.
-   Les rédacteurs et les demandeurs doivent spécifier uniquement des ressources locales. Les ressources locales sont des ensembles de fichiers dont le chemin d’accès absolu commence par une lettre de lecteur, et la lettre de lecteur ne peut pas être associée à un dossier monté sur un partage distant.
-   Le nombre maximal de clichés instantanés logiciels pour chaque volume est de 512. Toutefois, par défaut, vous ne pouvez conserver que 64 clichés instantanés utilisés par la fonctionnalité Clichés instantanés de dossiers partagés. Pour modifier la limite de la fonctionnalité clichés instantanés de dossiers partagés, utilisez la clé de Registre [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) .
-   L’infrastructure des composants de sauvegarde ne prend pas en charge la sauvegarde des ressources de cluster en tant que composants d’écriture. Pour sauvegarder des ressources de cluster, les applications doivent supposer que le chemin d’accès est local à un nœud de cluster particulier spécifié.
-   [!Note]  
    > Microsoft ne fournit pas de support technique pour les développeurs ou les professionnels de l’informatique pour l’implémentation des restaurations en ligne de l’état du système sur Windows (toutes les versions).

     

    Lors de la sauvegarde et de la récupération de l’état du système, la stratégie recommandée consiste à sauvegarder et à récupérer les volumes système et de démarrage en plus des fichiers énumérés par les Writers d’État du système.

    > [!Note]  
    > Les Writers d’État du système sont des enregistreurs dont l’attribut de [**\_ \_ type d’utilisation VSS**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) est défini sur VSS \_ ut \_ BOOTABLESYSTEMSTATE ou VSS \_ ut \_ SYSTEMSERVICE.

     

 

 
