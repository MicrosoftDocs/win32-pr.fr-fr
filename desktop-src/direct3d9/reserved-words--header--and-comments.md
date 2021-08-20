---
description: Le tableau ci-dessous montre les mots qui sont réservés et qui ne doivent pas être utilisés.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Mots réservés, en-tête et commentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f583084b3faa4777a5fe6031cc247fdb99c27cc1fb23c6a5676e60afe00aba20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044278"
---
# <a name="reserved-words-header-and-comments"></a>Mots réservés, en-tête et commentaires

Le tableau ci-dessous montre les mots qui sont réservés et qui ne doivent pas être utilisés.

| Mots réservés | Mots réservés | Mots réservés|
|------------------|----------|-----------|
| ARRAY            | DWORD    | UCHAR     |
| BINARY           | FLOAT    | ULONGLONG |
| \_ressource binaire | SDWORD   | UNICODE   |
| CHAR             | STRING   | WORD      |
| CSTRING          | SWORD    |           |
| DOUBLE           | TEMPLATE |           |



 

L’en-tête de longueur variable est obligatoire et doit se trouver au début du flux de données. L’en-tête contient les données suivantes.



| Type           | Obligatoire | Taille (en octets) | Valeur | Description                  |
|----------------|----------|-----------------|-------|------------------------------|
| Nombre magique   | x        | 4               | xof   |                              |
| Numéro de version | x        | 2               | 03    | Version majeure 3              |
|                |          |                 | 03    | Version mineure 3              |
| Type de format    | x        | 4               | txt   | Fichier texte                    |
|                |          |                 | bin   | Fichier binaire                  |
|                |          |                 | tzip  | Fichier texte compressé MSZip   |
|                |          |                 | bzip  | Fichier binaire compressé MSZip |
| Taille de la virgule flottante     | x        | 0064            |       | virgule flottante 64 bits                |
|                | x        | « 0032 »          |       | virgule flottante 32 bits                |



 

Les valeurs de la table sont délimitées par des guillemets pour attirer l’attention sur le nombre de caractères de chaque valeur. Ceux qui comportent 4 octets contiennent quatre caractères, ceux avec 2 octets contiennent deux caractères.

Les commentaires s’appliquent uniquement aux fichiers texte. Des commentaires peuvent apparaître n’importe où dans le flux de données. Un commentaire commence par deux barres obliques (//) de style C++ ou par un signe dièse ( \# ). Le commentaire s’exécute jusqu’à la nouvelle ligne suivante. L’exemple suivant montre des commentaires valides.


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Encodage de texte](text-encoding.md)
</dt> </dl>

 

 



