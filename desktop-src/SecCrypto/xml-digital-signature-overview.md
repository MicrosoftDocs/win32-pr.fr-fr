---
description: XML est une norme du secteur pour la description des données structurées. Une signature numérique XML est une représentation XML d’une signature numérique qui permet de vérifier l’origine et l’intégrité du document XML et des données référencées en externe.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Vue d’ensemble de la signature numérique XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519138"
---
# <a name="xml-digital-signature-overview"></a>Vue d’ensemble de la signature numérique XML

XML est une norme du secteur pour la description des données structurées. Une signature numérique XML est une représentation XML d’une [*signature numérique*](../secgloss/d-gly.md) qui permet de vérifier l’origine et l’intégrité du document XML et des données référencées en externe. Les signatures numériques XML peuvent être utilisées pour signer des données arbitraires, notamment un fragment ou un document XML, une page HTML, du texte brut ou des données codées en binaire, telles qu’un fichier JPEG.

Le format de signature numérique XML pris en charge par l’API de signature numérique CryptXML est spécifié par la recommandation du W3C sur la syntaxe et le traitement des signatures XML (deuxième édition).

La signature numérique CryptXML implémente la prise en charge des types de signature requis, des algorithmes de chiffrement, des algorithmes de canonisation et de la transformation enveloppée spécifiée.

Les développeurs peuvent étendre l’ensemble par défaut des algorithmes de chiffrement pris en charge par CryptXML en créant des dll d’extension de chiffrement. Les développeurs peuvent également créer leurs propres transformations personnalisées et algorithmes de canonisation en plus de l’API CryptXML. Les développeurs peuvent utiliser les API CryptXML avec les API de certificat Windows.

 

 
