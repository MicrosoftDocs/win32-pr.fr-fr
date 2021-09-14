---
description: L’échange de données réseau fournit des fonctions qui vous permettent de supprimer un partage, d’obtenir ou de définir des informations de partage ou d’énumérer des partages.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Gestion des partages DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa89b890c9cf2b140f669b5e4dfa556cd11f978d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122269"
---
# <a name="managing-dde-shares"></a>Gestion des partages DDE

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

L’échange de données réseau fournit des fonctions qui vous permettent de supprimer un partage, d’obtenir ou de définir des informations de partage ou d’énumérer des partages.




| Tâche | Procédure | 
|------|-----------|
| Supprimer un partage DDE | Utilisez la fonction <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> . | 
| Recevoir des informations sur le partage DDE | Utilisez la fonction <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> . | 
| Définir les informations de partage DDE | Utilisez la fonction <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> . | 
| Énumérer les partages DDE | Utilisez la fonction <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> . Vous pouvez également énumérer les partages DDE approuvés à l’aide de la fonction <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> .<br /> | 
| Énumérer les utilisateurs connectés | Utilisez la fonction <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> . | 
| Modifier le nom de partage DDE | Supprimez l’ancien partage et créez un nouveau partage.<ol><li>Récupérez les informations de partage à l’aide de <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</li><li>Supprimez le partage à l’aide de <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</li><li>Modifiez le membre <strong>lpszShareName</strong> de la structure <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> retournée par <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</li><li>Transmettez la structure <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> modifiée à <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</li></ol> | 




 

 

