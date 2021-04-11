---
description: Les prédicats de profondeur de dossier contrôlent l’étendue d’une recherche en spécifiant un chemin d’accès et s’il faut effectuer une traversée profonde ou superficielle.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Prédicats d’étendue et de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112431"
---
# <a name="scope-and-directory-predicates"></a>Prédicats d’étendue et de répertoire

Les prédicats de profondeur de dossier contrôlent l’étendue d’une recherche en spécifiant un chemin d’accès et s’il faut effectuer une traversée profonde ou superficielle. L’exemple suivant illustre la syntaxe des prédicats de profondeur de dossier :


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



Le prédicat est suivi d’un signe égal. Le chemin d’accès est indiqué entre guillemets simples et doit commencer par un protocole et un signe deux-points (par exemple,, `file:` `mapi:` ou `csc:` ). Le prédicat SCOPE effectue une traversée profonde du chemin d’accès, y compris tous les sous-dossiers, tandis que le prédicat de répertoire effectue un parcours superficiel uniquement du dossier spécifié. À l’instar des autres restrictions de langage SQL (SQL), vous pouvez spécifier plusieurs restrictions de profondeur de dossier dans une seule requête.

Pour interroger le catalogue local d’un ordinateur distant, incluez le nom de l’ordinateur avant le catalogue et un chemin d’accès UNC (Universal Naming Convention) sur l’ordinateur distant dans la clause SCOPE ou DIRECTORY.

## <a name="examples"></a>Exemples


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



L’exemple First SCOPE recherche le \\ \\ dossier de rapports C : Files et tous ses sous-dossiers. L’exemple de répertoire recherche uniquement dans le dossier racine les rapports C : \\ Files \\ .

> [!Note]  
> Les barres obliques inverses du système de fichiers ( \\ ) deviennent une barre oblique de style URL (parfois appelée barres obliques) (/).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[FROM, clause](-search-sql-from.md)
</dt> <dt>

[Clause WHERE](-search-sql-where.md)
</dt> </dl>

 

 



