---
description: Explique comment utiliser SignTool pour signer un fichier.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Utilisation de SignTool pour signer un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089026cde629278e5c6ac033164c2a9d26528917
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127417653"
---
# <a name="using-signtool-to-sign-a-file"></a>Utilisation de SignTool pour signer un fichier

la commande suivante signe le fichier nommé MyControl.exe à l’aide d’un [*certificat*](../secgloss/c-gly.md) stocké dans un fichier PFX (Personal Information Exchange) :

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

La commande suivante signe le fichier à l’aide d’un certificat stocké dans un fichier PFX protégé par mot de passe :

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> Veillez à protéger correctement le mot de passe.

 

La commande suivante signe et horodatage le fichier :

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> Pour plus d’informations sur l’horodatage d’un fichier après qu’il a déjà été signé, consultez [Ajout d’horodatages à des fichiers précédemment signés](adding-time-stamps-to-previously-signed-files.md).

 

La commande suivante signe le fichier à l’aide d’un certificat situé dans le magasin My, avec le nom d’objet My Company Publisher :

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

la commande suivante signe un contrôle ActiveX et fournit des informations qui sont affichées par Internet Explorer lorsque l’utilisateur est invité à installer le contrôle :

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

La commande suivante signe le fichier à l’aide d’un certificat dont les informations de [*clé privée*](../secgloss/p-gly.md) sont protégées par un module de chiffrement matériel. À titre d’exemple, supposons que le certificat appelé « My High-Value Certificate » dispose d’une clé privée installée dans un module de chiffrement matériel et que le certificat soit correctement installé.

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

La commande suivante signe le fichier à l’aide d’un certificat dont les informations de [*clé privée*](../secgloss/p-gly.md) sont protégées par un module de chiffrement matériel. Un magasin d’ordinateurs est spécifié pour le magasin de l' [*autorité de certification*](../secgloss/c-gly.md) (ca).

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

La commande suivante signe le fichier à l’aide d’un certificat stocké dans un fichier. Les informations de la clé privée sont protégées par un module de chiffrement matériel, et le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et le [*conteneur de clé*](../secgloss/k-gly.md) sont spécifiés par leur nom. Cette commande est utile si le certificat n’est pas installé correctement.

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

[SignTool](signtool.md) retourne le texte de ligne de commande qui indique le résultat de l’opération de signature. En outre, SignTool retourne un code de sortie de zéro pour une exécution réussie, un pour l’échec de l’exécution et deux pour l’exécution qui s’est terminée avec des avertissements.

Pour plus d’informations sur la vérification de la signature d’un fichier, consultez [utilisation de SignTool pour vérifier une signature de fichier](using-signtool-to-verify-a-file-signature.md). Pour plus d’informations sur l’ajout d’un horodatage si le fichier a déjà été signé, consultez [Ajout d’horodatages à des fichiers précédemment signés](adding-time-stamps-to-previously-signed-files.md). Pour plus d’informations sur [SignTool](signtool.md), consultez [SignTool](signtool.md).

 

 
