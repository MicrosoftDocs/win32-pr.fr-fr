---
description: En savoir plus sur le contrôle de version TSPI. Au fil du temps, différentes versions de TAPI, d’applications et de fournisseurs de services peuvent être générées.
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: Contrôle de version TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0a0663a1fcc685df8643c634ec627f669aafe8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123017"
---
# <a name="tspi-versioning"></a>Contrôle de version TSPI

Au fil du temps, différentes versions de TAPI, d’applications et de fournisseurs de services peuvent être générées. Ces nouvelles versions peuvent créer de nouvelles définitions, telles que des nouvelles fonctionnalités, de nouveaux membres dans les structures de données et de nouveaux champs de bits. Les numéros de version sont donc nécessaires pour indiquer comment interpréter diverses structures de données.

Pour permettre une interopérabilité optimale des différentes versions des applications, des versions de l’interface TAPI elle-même et des versions des fournisseurs de services par différents fournisseurs, Microsoft Telephony fournit un mécanisme de négociation de version simple pour les applications. Il existe deux versions différentes qui doivent être approuvées par l’interface TAPI et le fournisseur de services de téléphonie pour chaque périphérique de ligne. Le premier est le numéro de version du SPI de téléphonie de base et supplémentaire, appelé version de l' *interface TSPI*. L’autre est pour les extensions spécifiques au fournisseur, le cas échéant, et est appelée version de l' *extension*. Le format des structures de données et des types de données utilisés par les fonctionnalités de base et supplémentaires de TSPI est défini par la version de TSPI, tandis que la version d’extension détermine le format des structures de données définies par les extensions spécifiques au fournisseur.

Ces deux types de négociation de version sont gérés par deux procédures différentes : [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) est utilisé pour négocier la version de l’interface TSPI, et [**TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) est utilisé pour négocier la version de l’extension. La négociation de version d’extension peut être ignorée si les extensions ne sont pas souhaitées. Si ces plages entrées pendant la négociation se chevauchent, le fournisseur de services doit retourner une valeur dans la partie chevauchante de la plage en tant que résultat de la négociation. En règle générale, il doit s’agir de la valeur la plus élevée possible. Si les plages ne se chevauchent pas, les deux parties sont incompatibles et la fonction retourne une erreur.

Les résultats d’une négociation indiquent simplement que le fournisseur de services est disposé à fonctionner à un numéro de version particulier, mais ne valide pas le fournisseur de services. Par exemple, TAPI peut renégocier pour déterminer une version idéale après avoir négocié une version possible. La version de l’interface TSPI n’est validée que lorsqu’une ligne est ouverte à l’aide de [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) et qu’elle survivent jusqu’à la fermeture de l’appareil. La version de l’extension est validée lorsque la fonction [**TSPI \_ lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) est appelée, et survit jusqu’à ce que la sélection soit annulée en sélectionnant extension version zéro.

La sélection de la version de l’extension peut se produire plusieurs fois, y compris lorsqu’une version d’extension est en vigueur. Étant donné que le fournisseur de services est validé dans la version de l’extension, sa plage de versions prises en charge est limitée à cette version de l’extension. Par exemple, considérez un fournisseur de services qui est normalement compatible avec les versions d’extension 1,0 à 5,5. Si la version 3,0 est activée alors qu’un appelant tente de négocier une version comprise dans la plage 1,0 à 5,5, la négociation retourne 3,0.

Étant donné que TAPI négocie la version, vous pouvez mettre à niveau un fournisseur de services vers les nouvelles versions de l’interface sans avoir besoin de mettre à niveau l’interface TAPI. De même, TAPI peut être mis à niveau, tout en continuant à utiliser votre ancien fournisseur de services.

 

 
