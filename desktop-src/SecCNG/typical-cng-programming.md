---
description: L’API CNG implémente un modèle de fournisseur extensible qui vous permet de charger un fournisseur en spécifiant l’algorithme de chiffrement requis plutôt qu’un fournisseur particulier.
ms.assetid: a88a089b-4afe-4201-96f7-97f19bce18a1
title: Programmation CNG classique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1119da63ca1ea0613444b150914c06664f36c121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751660"
---
# <a name="typical-cng-programming"></a>Programmation CNG classique

L’API CNG implémente un modèle de fournisseur extensible qui vous permet de charger un fournisseur en spécifiant l’algorithme de chiffrement requis plutôt qu’un fournisseur particulier. L’avantage est qu’un fournisseur d’algorithme peut être remplacé ou mis à niveau et que vous n’aurez pas à modifier votre code de quelque façon que ce soit pour utiliser le nouveau fournisseur. En outre, si un algorithme est considéré comme non sécurisé à l’avenir, une version plus sécurisée de cet algorithme peut être installée sans affecter votre code. La plupart des API CNG requièrent un fournisseur ou un objet créé par un fournisseur.

Les étapes typiques de l’utilisation de l’API CNG pour les opérations primitives de chiffrement sont les suivantes :

1.  Ouverture du fournisseur d’algorithme
2.  Obtention ou définition des propriétés de l’algorithme
3.  Création ou importation d’une clé
4.  Exécution d’opérations de chiffrement
5.  Fermeture du fournisseur d’algorithme

Pour plus d’informations, consultez Exemples de programmation.

## <a name="opening-the-algorithm-provider"></a>Ouverture du fournisseur d’algorithme

La fonction [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) fournit un handle de fournisseur d’algorithme qui est utilisé dans les API CNG ultérieures, telles que [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) ou [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair).

## <a name="getting-or-setting-algorithm-properties"></a>Obtention ou définition des propriétés de l’algorithme

Vous pouvez utiliser le handle du fournisseur d’algorithme pour obtenir les détails d’implémentation de l’algorithme, tels que la taille de la clé ou le mode actuel de l’opération. Vous utilisez la fonction [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) pour obtenir des propriétés spécifiques.

Vous pouvez également modifier les propriétés de l’algorithme. Par exemple, si vous souhaitez utiliser le chaînage de chiffrement par bloc ECB avec AES, vous définissez la propriété **\_ \_ mode de chaînage bcrypt** d’un algorithme AES sur le **mode de \_ chaîne bcrypt \_ \_ BCE**. la propriété est affectée à toutes les clés AES créées à l’aide de ce handle d’algorithme, sans qu’il soit nécessaire de configurer chaque clé AES. Vous utilisez la fonction [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) pour modifier ces propriétés.

## <a name="creating-or-importing-a-key"></a>Création ou importation d’une clé

Selon le type d’algorithme que vous utilisez, vous devrez peut-être créer ou charger une clé. Par exemple, la fonction [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) prend un handle de clé pour le premier paramètre. Si vous souhaitez que cette fonction chiffre les données avec un algorithme de chiffrement symétrique tel qu’AES, vous devez d’abord obtenir une clé. La façon dont vous obtenez la clé dépend du type d’algorithme utilisé et de la source de la clé.

Vous pouvez créer des clés éphémères avec les fonctions [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) et [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) . Vous pouvez également importer des clés éphémères à partir d’un objet BLOB de mémoire avec les fonctions [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) et [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) .

Pour les clés persistantes, utilisez les fonctions de stockage de clés pour charger un fournisseur de stockage de clés, puis créez ou chargez les clés. Vous pouvez également utiliser ces fonctions pour créer ou charger des clés éphémères en transmettant la **valeur null** pour tous les noms de conteneurs. Pour plus d’informations sur les fonctions de stockage de clés, consultez [fonctions de stockage de clés CNG](cng-key-storage-functions.md).

## <a name="performing-cryptographic-operations"></a>Exécution d’opérations de chiffrement

Vous êtes maintenant prêt à effectuer l’opération de chiffrement, comme le chiffrement ou le déchiffrement des données à l’aide des fonctions [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) ou [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) , respectivement.

## <a name="closing-the-algorithm-provider"></a>Fermeture du fournisseur d’algorithme

Lorsque le fournisseur n’est plus nécessaire, vous devez passer le handle à la fonction [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) pour fermer le fournisseur. Cela amène le fournisseur à libérer toutes les ressources qui ont été allouées pour cette instance du fournisseur d’algorithme. Une fois qu’un descripteur de fournisseur est fermé, il ne peut pas être réutilisé.

Le chargement d’un fournisseur peut être un processus relativement fastidieux. Par conséquent, vous devez mettre en cache tous les descripteurs de fournisseur que vous référencerez plusieurs fois pendant la durée de vie de votre application.

## <a name="programming-examples"></a>Exemples de programmation

Les exemples suivants décrivent comment effectuer des opérations de chiffrement spécifiques à l’aide de CNG.

-   [Création d’un hachage avec CNG](creating-a-hash-with-cng.md)
-   [Signature de données avec CNG](signing-data-with-cng.md)
-   [Chiffrement des données avec CNG](encrypting-data-with-cng.md)

 

 



