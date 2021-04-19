---
description: Traitement des données
ms.assetid: 823615df-ce50-4e20-957a-f83d3be66658
title: Traitement des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbece449df36c2de88414f313d477b8a16ba896
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515314"
---
# <a name="processing-data"></a>Traitement des données

**Analyse des données multimédias**

Si votre filtre analyse les données multimédia, ne faites pas confiance aux en-têtes ou autres données autodescriptives dans le contenu. Par exemple, ne faites pas confiance aux valeurs de taille qui s’affichent dans les paquets AVI ou MPEG. Voici des exemples courants de ce type d’erreur :

-   Lecture de *n* octets de données, où la valeur de *n* provient du contenu, *sans vérifier la* taille réelle de la mémoire tampon.
-   Passage à un offset d’octet dans une mémoire tampon, sans vérifier que le décalage se situe dans la mémoire tampon.

Une autre classe d’erreurs courante implique de ne pas valider les descriptions de format trouvées dans le contenu. Par exemple :

-   Une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) peut être suivie d’une table de couleurs. La structure **BITMAPINFO,** est définie comme une structure **BITMAPINFOHEADER** suivie d’un tableau de valeurs **RGBQUAD** qui composent la table des couleurs. La taille du tableau est déterminée par la valeur de **biClrUsed**. Ne copiez jamais une table des couleurs dans un **BITMAPINFO,** sans vérifier d’abord la taille de la mémoire tampon allouée pour la structure **BITMAPINFO,** .
-   Une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) peut avoir des informations de format supplémentaires ajoutées à la structure. Le membre **cbSize** spécifie la taille des informations supplémentaires.

Lors de la connexion de code confidentiel, un filtre doit vérifier que toutes les structures de format sont bien formées et contiennent des valeurs raisonnables. Si ce n’est pas le cas, refusez la connexion. Dans le code qui valide la structure de format, soyez particulièrement vigilant avec le débordement arithmétique. Par exemple, dans un **BITMAPINFOHEADER**, la largeur et la hauteur sont des valeurs **longues** de 32 bits, mais la taille de l’image (qui est une fonction du produit des deux) n’est qu’une valeur **DWORD** .

Si les données de format de la source sont plus volumineuses que votre mémoire tampon allouée, ne tronquez pas les données sources afin de les copier dans votre mémoire tampon. Cela permet de créer une structure dont la taille implicite est supérieure à sa taille réelle. Par exemple, un en-tête de bitmap peut spécifier une table de palette qui n’existe plus. Au lieu de cela, réallouez la mémoire tampon ou faites simplement échouer la connexion.

**Erreurs pendant la diffusion en continu**

Lorsque le graphique est en cours d’exécution, si votre filtre reçoit du contenu incorrect, il doit mettre fin à la diffusion en continu. Effectuez les actions suivantes :

-   Retourne un code d’erreur de la part de **Receive**.
-   Appelez [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur le filtre en aval.
-   Appelez [**CBaseFilter :: NotifyEvent**](cbasefilter-notifyevent.md) pour poster un événement [**EC \_ ERRORABORT**](ec-errorabort.md) .

**Modifications de format**

Plusieurs mécanismes existent pour que les filtres modifient les formats mi-flux. Chacune d’elles implique plusieurs étapes, ce qui crée le potentiel pour les fausses acceptations. Si votre filtre reçoit une demande de modification de format dynamique, il doit soit rejeter la demande, soit honorer le nouveau format à son arrivée. De même, ne changez jamais de format à moins que l’autre filtre n’accepte. Pour plus d’informations, consultez [modifications de format dynamique](dynamic-format-changes.md).

 

 
