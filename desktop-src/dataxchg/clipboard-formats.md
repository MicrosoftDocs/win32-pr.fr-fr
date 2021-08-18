---
title: Formats du presse-papiers
description: Une fenêtre peut placer plusieurs objets dans le presse-papiers, chacun représentant les mêmes informations dans un format de presse-papiers différent. Les utilisateurs n’ont pas besoin de connaître les formats du presse-papiers utilisés pour un objet dans le presse-papiers.
ms.assetid: fe42baec-6b00-4816-b379-7f335da8a197
keywords:
- presse-papiers, formats
- presse-papiers, fenêtres
- presse-papiers, formats standard
- presse-papiers, formats enregistrés
- presse-papiers, formats synthétisés
- formats de presse-papiers standard
- formats de presse-papiers inscrits
- formats de presse-papiers synthétisés
- formats du presse-papiers Cloud
- formats d’historique du presse-papiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6bd2dc9dda8c8ccecd164123af68865005d9d28d328ce5489abf23926113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991339"
---
# <a name="clipboard-formats"></a>Formats du presse-papiers

Une fenêtre peut placer plusieurs objets dans le presse-papiers, chacun représentant les mêmes informations dans un format de presse-papiers différent. Les utilisateurs n’ont pas besoin de connaître les formats du presse-papiers utilisés pour un objet dans le presse-papiers.

Les rubriques suivantes décrivent les formats du presse-papiers.

-   [Formats de presse-papiers standard](#standard-clipboard-formats)
-   [Formats de presse-papiers inscrits](#registered-clipboard-formats)
-   [Formats de presse-papiers privés](#private-clipboard-formats)
-   [Plusieurs formats de presse-papiers](#multiple-clipboard-formats)
-   [Formats de presse-papiers synthétisés](#synthesized-clipboard-formats)
-   [Presse-papiers du Cloud et formats d’historique du presse-papiers](#cloud-clipboard-and-clipboard-history-formats)

## <a name="standard-clipboard-formats"></a>Formats de presse-papiers standard

Les formats de presse-papiers définis par le système sont appelés *formats de presse-papiers standard*. Ces formats de presse-papiers sont décrits dans les [**formats de presse-papiers standard**](standard-clipboard-formats.md).

## <a name="registered-clipboard-formats"></a>Formats de presse-papiers inscrits

De nombreuses applications fonctionnent avec des données qui ne peuvent pas être traduites dans un format de presse-papiers standard sans perte d’informations. Ces applications peuvent créer leurs propres formats de presse-papiers. Un format de presse-papiers qui est défini par une application est appelé [format de presse-papiers inscrit](#registered-clipboard-formats). Par exemple, si une application de traitement de texte copiait du texte mis en forme dans le presse-papiers à l’aide d’un format de texte standard, les informations de mise en forme seraient perdues. La solution consisterait à inscrire un nouveau format de presse-papiers, par exemple RTF (Rich Text Format).

Pour inscrire un nouveau format de presse-papiers, utilisez la fonction [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) . Cette fonction prend le nom du format et retourne une valeur entière non signée qui représente le format de presse-papiers inscrit. Pour récupérer le nom du format du presse-papiers inscrit, transmettez la valeur de l’entier non signé à la fonction [**GetClipboardFormatName**](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea) .

Si plusieurs applications inscrivent un format de presse-papiers avec exactement le même nom, le format du presse-papiers n’est inscrit qu’une seule fois. Les deux appels à la fonction [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) retournent la même valeur. De cette façon, deux applications différentes peuvent partager des données à l’aide d’un format de presse-papiers inscrit.

## <a name="private-clipboard-formats"></a>Formats de presse-papiers privés

Une application peut identifier un format de presse-papiers privé en définissant une valeur dans la plage **CF \_ PRIVATEFIRST** via **CF \_ PRIVATELAST**. Une application peut utiliser un format de presse-papiers privé pour un format de données défini par l’application qui n’a pas besoin d’être inscrit auprès du système.

Les descripteurs de données associés aux formats de presse-papiers privés ne sont pas automatiquement libérés par le système. Si votre Windows utilise des formats de presse-papiers privés, vous pouvez utiliser le message [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) pour libérer toutes les ressources associées qui ne sont plus nécessaires.

Pour plus d’informations sur le message [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) , consultez [propriété du presse-papiers](clipboard-operations.md).

Une application peut placer des handles de données dans le presse-papiers en définissant un format privé dans la plage **CF \_ GDIOBJFIRST** via **CF \_ GDIOBJLAST**. lors de l’utilisation de valeurs dans cette plage, le descripteur de données n’est pas un handle vers un objet Windows Graphics Device Interface (GDI), mais est un handle alloué par la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) avec l' \_ indicateur GMEM moveon. Lorsque le presse-papiers est vidé, le système supprime automatiquement l’objet à l’aide de la fonction [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .

## <a name="multiple-clipboard-formats"></a>Plusieurs formats de presse-papiers

Une fenêtre peut placer plusieurs objets Clipboard dans le presse-papiers, chacun représentant les mêmes informations dans un format de presse-papiers différent. Lorsque vous placez des informations dans le presse-papiers, la fenêtre doit fournir les données dans le plus grand nombre possible de formats. Pour connaître le nombre de formats actuellement utilisés dans le presse-papiers, appelez la fonction [**CountClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats) .

Les formats de presse-papiers qui contiennent le plus d’informations doivent être placés en premier dans le presse-papiers, suivis par des formats moins descriptifs. Une fenêtre qui colle des informations à partir du presse-papiers récupère généralement un objet du presse-papiers dans le premier format reconnu. Étant donné que les formats de presse-papiers sont énumérés dans l’ordre dans lequel ils sont placés dans le presse-papiers, le premier format reconnu est également le plus descriptif.

Par exemple, supposons qu’un utilisateur copie un texte stylisé à partir d’un document de traitement de texte. La fenêtre contenant le document peut d’abord placer des données dans le presse-papiers dans un format enregistré, tel que RTF. Par la suite, la fenêtre placerait des données dans le presse-papiers dans un format moins descriptif, tel que texte (**\_ texte de CF**).

Lorsque le contenu du presse-papiers est collé dans une autre fenêtre, la fenêtre récupère les données au format le plus descriptif qu’il reconnaît. Si la fenêtre reconnaît le format RTF, les données correspondantes sont collées dans le document. Dans le cas contraire, les données de texte sont collées dans le document et les informations de mise en forme sont perdues.

## <a name="synthesized-clipboard-formats"></a>Formats de presse-papiers synthétisés

Le système convertit implicitement les données entre certains formats de presse-papiers : si une fenêtre demande des données dans un format qui ne se trouve pas dans le presse-papiers, le système convertit un format disponible au format demandé. Le système peut convertir les données comme indiqué dans le tableau suivant.



| Format de Presse-papiers     | Format de conversion    |
|----------------------|----------------------|
| **\_bitmap cf**       | **CF \_ DIB**          |
| **\_bitmap cf**       | **CF \_ DIBV5**        |
| **CF \_ DIB**          | **\_bitmap cf**       |
| **CF \_ DIB**          | **\_palette cf**      |
| **CF \_ DIB**          | **CF \_ DIBV5**        |
| **CF \_ DIBV5**        | **\_bitmap cf**       |
| **CF \_ DIBV5**        | **CF \_ DIB**          |
| **CF \_ DIBV5**        | **\_palette cf**      |
| **CF \_ ENHMETAFILE**  | **CF \_ MetaFilePict** |
| **CF \_ MetaFilePict** | **CF \_ ENHMETAFILE**  |
| **CF \_ OEMTEXT**      | **\_texte cf**         |
| **CF \_ OEMTEXT**      | **CF \_ UNICODETEXT**  |
| **\_texte cf**         | **CF \_ OEMTEXT**      |
| **\_texte cf**         | **CF \_ UNICODETEXT**  |
| **CF \_ UNICODETEXT**  | **CF \_ OEMTEXT**      |
| **CF \_ UNICODETEXT**  | **\_texte cf**         |



 

Si le système fournit une conversion automatique de type pour un format de presse-papiers particulier, il n’y a aucun avantage à placer le ou les formats de conversion dans le presse-papiers.

Si le système fournit une conversion automatique de type pour un format de presse-papiers particulier et que vous appelez [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) pour énumérer les formats de données du presse-papiers, le système énumère d’abord le format qui se trouve dans le presse-papiers, suivi des formats dans lesquels il peut être converti.

Lors de la copie de bitmaps, il est préférable de placer le format **CF \_ DIB** ou **CF \_ DIBV5** dans le presse-papiers. Cela est dû au fait que les couleurs d’une bitmap dépendante de l’appareil (**\_ bitmap CF**) sont relatives à la palette du système, ce qui peut changer avant le collage de l’image bitmap. Si le format de **CF \_ DIB** ou **CF \_ DIBV5** se trouve dans le presse-papiers et qu’une fenêtre demande le format de **\_ bitmap CF** , le système restitue la bitmap indépendante du périphérique (DIB) à ce moment-là.

Si vous placez le format de **\_ bitmap CF** dans le presse-papiers (et non dans **CF \_ DIB**), le système restitue le format de presse-papiers **\_ DIB** ou **CF \_ DIBV5** dès que le presse-papiers est fermé. Cela permet de s’assurer que la palette correcte est utilisée pour générer le DIB. Si vous placez le format **CF \_ DIBV5** avec les informations d’espace de couleurs de bitmap dans le presse-papiers, le système convertit les bits de bitmap de l’espace de couleurs de la bitmap dans l’espace de couleurs sRVB lorsque **CF \_ DIB** ou **CF \_ DIBV5** est demandé. Si **CF \_ DIBV5** est demandé quand il n’y a pas d’informations sur l’espace colorimétrique dans le presse-papiers, le système retourne des informations sur l’espace colorimétrique sRVB dans la structure [**BITMAPV5HEADER**](/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header) . Les conversions entre les autres formats de presse-papiers se produisent à la demande.

Si le presse-papiers contient des données au format de la **\_ palette CF** , l’application doit utiliser les fonctions [**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette) et [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) pour réaliser toutes les autres données du presse-papiers par rapport à cette palette logique.

Il existe deux formats de presse-papiers pour les sous-fichiers : **CF \_ ENHMETAFILE** et **CF \_ MetaFilePict**. spécifiez **cf \_ ENHMETAFILE** pour les sous-fichiers améliorés et **cf \_ METAFILEPICT** pour Windows les sous-fichiers.

## <a name="cloud-clipboard-and-clipboard-history-formats"></a>Presse-papiers du Cloud et formats d’historique du presse-papiers

certaines versions de Windows incluent le [presse-papiers Cloud](/windows/whats-new/whats-new-windows-10-version-1809#cloud-clipboard), qui conserve un historique des éléments de données du presse-papiers récents et peut les synchroniser entre les appareils de l’utilisateur.
si vous ne souhaitez pas que les données que votre application place dans le presse-papiers soient incluses dans l’historique du presse-papiers ou synchronisées avec d’autres appareils, votre application peut contrôler ce comportement en plaçant des données dans certains [formats de presse-papiers inscrits](#registered-clipboard-formats) dont les noms sont connus du système Windows :

- **ExcludeClipboardContentFromMonitorProcessing** : Placez toutes les données dans le presse-papiers dans ce format pour empêcher que tous les formats du presse-papiers soient inclus dans l’historique du presse-papiers ou synchronisés avec les autres appareils de l’utilisateur.
- **CanIncludeInClipboardHistory** : Placez une valeur **[DWORD](../WinProg/windows-data-types.md)** sérialisée de zéro dans le presse-papiers dans ce format pour empêcher l’inclusion de tous les formats du presse-papiers dans l’historique du presse-papiers, ou placez la valeur un à la place pour demander explicitement que l’élément du presse-papiers soit inclus dans l’historique du presse-papiers. Cela n’affecte pas la synchronisation sur les autres appareils de l’utilisateur.
- **CanUploadToCloudClipboard** : Placez une valeur **[DWORD](../WinProg/windows-data-types.md)** sérialisée de zéro dans le presse-papiers dans ce format pour empêcher la synchronisation de tous les formats du presse-papiers avec les autres appareils de l’utilisateur, ou placez la valeur un à la place pour demander explicitement que l’élément du presse-papiers soit synchronisé avec d’autres appareils. Cela n’affecte pas l’historique du presse-papiers de l’appareil local.

Comme pour les autres formats de presse-papiers enregistrés, vous devrez utiliser la fonction [**RegisterClipboardFormat**](
/windows/win32/api/winuser/nf-winuser-registerclipboardformata) pour obtenir une valeur entière non signée qui identifie chacun des 3 formats ci-dessus.