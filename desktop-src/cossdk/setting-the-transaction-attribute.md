---
description: Vous pouvez définir les attributs de transaction manuellement à l’aide de l’outil d’administration Services de composants, ou vous pouvez ajouter la prise en charge de la programmation des transactions lors de l’écriture de votre composant.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Définition de l’attribut de transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0690a50f79c77a18b089cec1865dfbb9e7f428
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310969"
---
# <a name="setting-the-transaction-attribute"></a>Définition de l’attribut de transaction

Vous pouvez définir les attributs de transaction manuellement à l’aide de l’outil d’administration Services de composants, ou vous pouvez ajouter la prise en charge de la programmation des transactions lors de l’écriture de votre composant.

Pour plus d’informations sur les valeurs des attributs de transaction, consultez [Configuration des transactions](configuring-transactions.md).

**Pour définir la valeur de l’attribut à l’aide de l’outil d’administration Services de composants**

1.  Dans l’arborescence de la console, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **transactions** .

3.  Sous **prise en charge des transactions**, sélectionnez l’option correspondant à la valeur de votre choix. La valeur par défaut de tous les composants n’est **pas prise en charge**.

4.  Cliquez sur **OK**.

Vous devez répéter cette procédure pour chaque composant.

## <a name="to-set-the-attribute-value-programmatically"></a>Pour définir la valeur de l’attribut par programmation

les programmeurs qui utilisent Microsoft Visual Basic peuvent définir l’attribut de transaction avec **MTSTransactionMode**, une propriété de module de classe pour les projets ActiveX DLL. Visual Basic mappe votre sélection à la valeur d’attribut de transaction COM+ équivalente et publie la valeur dans la bibliothèque de types de votre composant.

Le tableau suivant mappe chaque valeur de constante **MTSTransactionMode** à sa valeur de transaction com+ équivalente.



| MTSTransactionMode constante)         | Valeur de la transaction COM+             |
|-------------------------------------|------------------------------------|
| NotAnMTSObject (par défaut)<br/> | Désactivé<br/>                |
| Notransactions<br/>           | Non pris en charge (par défaut)<br/> |
| RequiresTransaction <br/>     | Obligatoire<br/>                |
| UsesTransaction <br/>         | Prise en charge<br/>               |
| RequiresNewTransaction <br/>  | Nouveau requis<br/>            |



 

Vous pouvez également accéder par programme à la propriété **MTSTransactionMode** à l’aide de l’API bibliothèque d’administration com+.

 

 




