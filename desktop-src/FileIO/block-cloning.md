---
description: Une opération de clonage de bloc indique au système de fichiers de copier une plage d’octets de fichier pour le compte d’une application.
ms.assetid: E18E8D79-3985-40B8-A4C5-A73A21E5C527
title: Clonage de bloc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33aa1c1eee693b6ed4b502aedc6da6176ece3e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530009"
---
# <a name="block-cloning"></a>Clonage de bloc

Une opération de *clonage de bloc* indique au système de fichiers de copier une plage d’octets de fichier pour le compte d’une application. Le fichier de destination peut être le même que le fichier source, ou être différent de celui-ci.

Un système de fichiers gère les mappages de [clusters et d’étendues](clusters-and-extents.md)et peut être en mesure d’effectuer la copie en modifiant le numéro de cluster virtuel (VCN) en mappages de nombre de clusters logiques (LCN) comme une opération de métadonnées à faible coût, au lieu de lire et d’écrire les données du fichier sous-jacent. Cela permet à la copie de s’exécuter plus rapidement et génère moins d’e/s sur le stockage sous-jacent. En outre, plusieurs fichiers peuvent maintenant partager des clusters logiques après le clone de bloc, ce qui évite de stocker les clusters identiques plusieurs fois sur le disque.

Une opération de clonage de bloc n’interrompt pas l’isolation fournie entre les fichiers. Une fois le clone de bloc terminé, les écritures dans le fichier source n’apparaissent pas dans la destination, ou vice versa.

Le clonage de bloc est disponible uniquement sur le type de [système de fichiers ReFS](/windows/desktop/w8cookbook/resilient-file-system--refs-) à partir de Windows Server 2016.

## <a name="block-cloning-on-refs"></a>Clonage de bloc sur ReFS

ReFS sur Windows Server 2016 implémente le clonage de bloc en remappant les clusters logiques (c’est-à-dire les emplacements physiques sur un volume) de la région source vers la région de destination. Il utilise ensuite un mécanisme d’allocation sur écriture pour garantir l’isolement entre ces régions. Les régions source et de destination peuvent être dans des fichiers identiques ou différents.

Cette implémentation requiert que les offsets de fichier de début et de fin soient alignés sur les limites du cluster. Dans ReFS sur Windows Server 2016, les clusters ont une taille de 4 Ko par défaut, mais peuvent éventuellement avoir la valeur 64 Ko. La taille du cluster est un paramètre au niveau du volume défini au moment de la mise en forme.

## <a name="restrictions-and-remarks"></a>Restrictions et remarques

-   Les régions source et de destination doivent commencer et se terminer à une limite de cluster.
-   La taille de la région clonée doit être inférieure à 4 Go.
-   La région de destination ne doit pas s’étendre au-delà de la fin du fichier. Si l’application souhaite étendre la destination avec des données clonées, elle doit d’abord appeler [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).
-   Si les régions source et de destination se trouvent dans le même fichier, elles ne doivent pas se chevaucher. (L’application peut se poursuivre en fractionnant l’opération de clonage de bloc en plusieurs clones de bloc qui ne se chevauchent plus.)
-   Les fichiers source et de destination doivent se trouver sur le même volume ReFS.
-   Les fichiers source et de destination doivent avoir le même paramètre [**flux d’intégrité**](file-attribute-constants.md) (autrement dit, les flux d’intégrité doivent être activés dans les deux fichiers ou désactivés dans les deux fichiers).
-   Si le fichier source est partiellement alloué, le fichier de destination doit l’être également.
-   L’opération de clonage de bloc interrompt les verrous opportunistes partagés (également appelés [verrous opportunistes de niveau 2](types-of-opportunistic-locks.md)).
-   Le volume ReFS doit avoir été formaté avec Windows Server 2016 et, si le clustering de basculement Windows est en cours d’utilisation, le niveau fonctionnel de clustering doit avoir été Windows Server 2016 ou une version ultérieure au format heure.

## <a name="example"></a>Exemple

Supposons que nous ayons deux fichiers, X et Y, où chaque fichier est composé de 3 régions distinctes. Chaque région de fichier est stockée dans une région distincte du volume. Le système de fichiers stocke la connaissance que chacune de ces régions de volume est référencée dans une région de fichier :

![avant le clonage](images/before-clone.png)

Supposons à présent qu’une application génère une opération de clonage de bloc dans le fichier X, sur les régions de fichier A et B, vers le fichier Y à l’offset où E est actuellement. L’état du système de fichiers suivant se produit :

![après le clonage](images/after-clone.png)

Les données dans les régions A et B ont été dupliquées du fichier X vers le fichier Y en modifiant les mappages VCN à LCN au sein du volume ReFS. Les étendues de disque qui sauvegardent les régions A et B n’ont pas été lues, et les étendues de disque sauvegardaient les anciennes régions E et F remplacées pendant l’opération.

Les fichiers X et Y partagent désormais des clusters logiques sur le disque. Cela se répercute dans le nombre de références indiqué dans le tableau. Le partage se traduit par une consommation de capacité de volume inférieure à celle des régions A et B qui étaient dupliquées sur le volume sous-jacent.

Supposons à présent que l’application remplace la région A dans le fichier X. ReFS crée une copie dupliquée d’un, que nous appelons maintenant G. ReFS, puis mappe G dans le fichier X et applique la modification. Cela permet de préserver l’isolation entre les fichiers. Les décomptes de références sont mis à jour de manière appropriée :

![après la modification de l’écriture](images/after-modifying-write.png)

Après la modification de l’écriture, la région B est toujours partagée sur le disque. Notez que si la région A avait été plus grande qu’un cluster, seul le cluster modifié aurait été dupliqué, et la partie restante aurait continué à être partagée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**DUPLIQUer les \_ données d’étendues \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-duplicate_extents_data)
</dt> <dt>

[**FSCTL \_ les \_ Extensions dupliquées dans le \_ \_ fichier**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)
</dt> </dl>

 

 
