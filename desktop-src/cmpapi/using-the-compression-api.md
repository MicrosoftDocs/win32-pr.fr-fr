---
description: De nombreuses applications doivent utiliser la compression et la décompression des données sans perte. l’api de compression simplifie cela en exposant Windows algorithmes de compression par le biais d’une API publique.
ms.assetid: D603A7DE-D4A1-4515-9702-B03C81504661
title: Utilisation de l’API de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01eff163f4ea1ccf03e1cd4ac9cb16a26afeb265
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918604"
---
# <a name="using-the-compression-api"></a>Utilisation de l’API de compression

De nombreuses applications doivent utiliser la compression et la décompression des données sans perte. l’api de compression simplifie cela en exposant Windows algorithmes de compression par le biais d’une API publique. Chaque algorithme de compression a un ensemble de propriétés qui contrôle son comportement. L’API de compression expose une interface qui permet au développeur de définir ou d’interroger les valeurs de ces propriétés. Toutes les propriétés des algorithmes de compression pris en charge ont des valeurs par défaut qui représentent les valeurs couramment utilisées de ces propriétés. Si une propriété est requise pour la compression et la décompression, les valeurs par défaut sont identiques, ce qui garantit que des valeurs identiques sont utilisées pour la compression et la décompression.

## <a name="selecting-the-compression-algorithm"></a>Sélection de l’algorithme de compression

Une fois qu’un développeur a décidé qu’une application a besoin de compresser ou de décompresser les données, l’étape suivante consiste à choisir un algorithme de compression. Cela peut dépendre de tests pour trouver la combinaison optimale de vitesse, de taux de compression et de mémoire requise pour une application particulière. La liste suivante fournit une comparaison relative des algorithmes de compression actuellement pris en charge par l’API de compression. Toutes les options ne sont pas disponibles pour chaque algorithme de compression, et la comparaison est approximative, car les performances peuvent dépendre des données d’entrée.

XPRESS (**compresser l' \_ algorithme \_ Xpress**)

-   Très rapide avec des exigences de ressources insuffisantes
-   Taux de compression moyen
-   Vitesses de compression et de décompression élevées
-   Mémoire insuffisante
-   Prend en charge l’option de **\_ niveau de \_ classe \_ d’informations compress** disponible dans l’énumération de [**\_ \_ classe d’informations compress**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . La valeur par défaut est **(DWORD) 0**. Pour certaines données, la valeur **(DWORD) 1** peut améliorer le taux de compression avec une vitesse de compression légèrement inférieure.

Codage XPRESS avec Huffman (**compression d' \_ algorithme \_ Xpress \_ Huff**)

-   Le taux de compression est plus élevé que **compresser l' \_ algorithme \_ Xpress**
-   Taux de compression moyen
-   Vitesses de compression moyenne à élevée et de décompression
-   Mémoire insuffisante
-   Prend en charge l’option **compresser les \_ données de \_ \_ niveau classe** dans l’énumération de [**\_ \_ classe d’informations compress**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . La valeur par défaut est **(DWORD) 0**. Pour certaines données, la valeur **(DWORD) 1** peut améliorer le taux de compression avec une vitesse de compression légèrement inférieure.

MSZIP (**compresser l' \_ algorithme \_ MSZIP**)

-   Utilise plus de ressources qu’un **\_ algorithme compress \_ Xpress \_ Huff**
-   Génère un bloc compressé similaire à la RFC 1951.
-   Taux de compression moyen à élevé
-   Vitesse de compression moyenne et vitesse de décompression élevée
-   Mémoire moyenne requise

LZMS (**compresser l' \_ algorithme \_ LZMS**)

-   Bon algorithme si la taille des données à compresser est supérieure à 2 Mo.
-   Taux de compression élevé
-   Vitesse de compression faible et vitesse de décompression élevée
-   Exigence de mémoire moyenne à élevée
-   Prend en charge l’option de **taille de bloc de \_ classe d’informations \_ \_ \_ Compress** dans l’énumération de [**\_ \_ classe d’informations compress**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . Une taille minimale de 1 Mo est suggérée pour obtenir un meilleur taux de compression.

## <a name="deciding-which-compression-api-mode-to-use"></a>Choix du mode d’API de compression à utiliser

Une fois que le développeur a sélectionné l’algorithme de compression, la décision suivante est celle des deux modes de l’API de compression à utiliser : mode mémoire tampon ou mode bloc. Le mode mémoire tampon a été développé pour une utilisation simplifiée et est recommandé dans la plupart des cas.

Le mode mémoire tampon fractionne automatiquement la mémoire tampon d’entrée en blocs d’une taille appropriée pour l’algorithme de compression sélectionné. Le mode mémoire tampon met en forme et stocke automatiquement la taille de la mémoire tampon non compressée dans la mémoire tampon compressée. La taille de la mémoire tampon compressée n’est pas enregistrée automatiquement et l’application doit l’enregistrer pour la décompression. N’incluez pas l’indicateur **Compress \_ RAW** dans le paramètre *Algorithm* lorsque vous appelez [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) et [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) pour utiliser le mode buffer. Pour obtenir un exemple de code d’une application en mode mémoire tampon, consultez la section utilisation de l' [API de compression en mode mémoire tampon](using-the-compression-api-in-buffer-mode.md) .

Le mode blocage permet au développeur de contrôler la taille du bloc, mais nécessite davantage de travail par l’application. Lors de l’utilisation du mode bloc, l’application doit scinder les données d’entrée en éléments de taille appropriée lors de la compression, puis replacer les parties lors de la décompression. Le mode bloc échoue si la taille de la mémoire tampon d’entrée est supérieure à la taille de bloc interne de l’algorithme de compression. La taille de bloc interne est de 32 Ko pour MSZIP et 1 Go pour les algorithmes de compression XPRESS. La taille de bloc interne pour LZMS peut être configurée jusqu’à 64 Go avec une augmentation correspondante de l’utilisation de la mémoire. La taille de la mémoire tampon compressée n’est pas enregistrée automatiquement, et l’application doit également l’enregistrer pour la décompression. La valeur du paramètre *UncompressedBufferSize* de la [**décompression**](/windows/desktop/api/compressapi/nf-compressapi-decompress) doit être exactement égale à la taille d’origine des données non compressées, et pas seulement à la taille de la mémoire tampon de sortie. Cela signifie que votre application doit enregistrer la taille d’origine exacte des données non compressées, ainsi que les données compressées et la taille compressée, lors de l’utilisation du mode bloc. Incluez l’indicateur de **compression \_ brute** dans le paramètre d' *algorithme* lorsque vous appelez à la fois [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) et [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) pour utiliser le mode bloc. Pour obtenir un exemple de code d’une application en mode bloc, consultez la section utilisation de l' [API de compression en mode bloc](using-the-compression-api-in-block-mode.md) .

## <a name="custom-memory-allocation"></a>Allocation de mémoire personnalisée

Les applications de mémoire tampon et en mode bloc ont la possibilité de spécifier une routine d’allocation de mémoire personnalisée quand elles appellent [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) et [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor). Le paramètre *AllocationRoutines* spécifie la structure des [**\_ \_ routines d’allocation de compression**](/windows/desktop/api/compressapi/ns-compressapi-compress_allocation_routines) qui contient la routine d’allocation de mémoire. L’application peut ensuite définir la taille de bloc pour le compresseur à l’aide de [**SetCompressorInformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation). Consultez la section [utilisation de l’API de compression en mode bloc](using-the-compression-api-in-block-mode.md) pour obtenir un exemple de routine d’allocation personnalisée simple.

 

 



