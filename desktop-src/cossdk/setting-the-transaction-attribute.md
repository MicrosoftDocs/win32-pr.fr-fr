---
description: Vous pouvez définir les attributs de transaction manuellement à l’aide de l’outil d’administration Services de composants, ou vous pouvez ajouter la prise en charge de la programmation des transactions lors de l’écriture de votre composant.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Définition de l’attribut de transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0690a50f79c77a18b089cec1865dfbb9e7f428
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111278"
---
# <a name="setting-the-transaction-attribute"></a><span data-ttu-id="d8425-103">Définition de l’attribut de transaction</span><span class="sxs-lookup"><span data-stu-id="d8425-103">Setting the Transaction Attribute</span></span>

<span data-ttu-id="d8425-104">Vous pouvez définir les attributs de transaction manuellement à l’aide de l’outil d’administration Services de composants, ou vous pouvez ajouter la prise en charge de la programmation des transactions lors de l’écriture de votre composant.</span><span class="sxs-lookup"><span data-stu-id="d8425-104">You can set transaction attributes manually by using the Component Services administrative tool, or you can add programmatic support for transactions when you write your component.</span></span>

<span data-ttu-id="d8425-105">Pour plus d’informations sur les valeurs des attributs de transaction, consultez [Configuration des transactions](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="d8425-105">For more on transaction attribute values, see [Configuring Transactions](configuring-transactions.md).</span></span>

<span data-ttu-id="d8425-106">**Pour définir la valeur de l’attribut à l’aide de l’outil d’administration Services de composants**</span><span class="sxs-lookup"><span data-stu-id="d8425-106">**To set the attribute value by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="d8425-107">Dans l’arborescence de la console, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="d8425-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="d8425-108">Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **transactions** .</span><span class="sxs-lookup"><span data-stu-id="d8425-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="d8425-109">Sous **prise en charge des transactions**, sélectionnez l’option correspondant à la valeur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="d8425-109">Under **Transaction support**, select the option for the value you want.</span></span> <span data-ttu-id="d8425-110">La valeur par défaut de tous les composants n’est **pas prise en charge**.</span><span class="sxs-lookup"><span data-stu-id="d8425-110">The default value for all components is **Not Supported**.</span></span>

4.  <span data-ttu-id="d8425-111">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8425-111">Click **OK**.</span></span>

<span data-ttu-id="d8425-112">Vous devez répéter cette procédure pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="d8425-112">You must repeat this procedure for each component.</span></span>

## <a name="to-set-the-attribute-value-programmatically"></a><span data-ttu-id="d8425-113">Pour définir la valeur de l’attribut par programmation</span><span class="sxs-lookup"><span data-stu-id="d8425-113">To set the attribute value programmatically</span></span>

<span data-ttu-id="d8425-114">Les programmeurs qui utilisent Microsoft Visual Basic peuvent définir l’attribut de transaction avec **MTSTransactionMode**, une propriété de module de classe pour les projets DLL ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d8425-114">Programmers using Microsoft Visual Basic can set the transaction attribute with **MTSTransactionMode**, a class module property for ActiveX DLL projects.</span></span> <span data-ttu-id="d8425-115">Visual Basic mappe votre sélection à la valeur d’attribut de transaction COM+ équivalente et publie la valeur dans la bibliothèque de types de votre composant.</span><span class="sxs-lookup"><span data-stu-id="d8425-115">Visual Basic maps your selection to the equivalent COM+ transaction attribute value and publishes the value in your component's type library.</span></span>

<span data-ttu-id="d8425-116">Le tableau suivant mappe chaque valeur de constante **MTSTransactionMode** à sa valeur de transaction com+ équivalente.</span><span class="sxs-lookup"><span data-stu-id="d8425-116">The following table maps each **MTSTransactionMode** constant value to its equivalent COM+ transaction value.</span></span>



| <span data-ttu-id="d8425-117">MTSTransactionMode constante)</span><span class="sxs-lookup"><span data-stu-id="d8425-117">MTSTransactionMode constant</span></span>         | <span data-ttu-id="d8425-118">Valeur de la transaction COM+</span><span class="sxs-lookup"><span data-stu-id="d8425-118">COM+ transaction value</span></span>             |
|-------------------------------------|------------------------------------|
| <span data-ttu-id="d8425-119">NotAnMTSObject (par défaut)</span><span class="sxs-lookup"><span data-stu-id="d8425-119">NotAnMTSObject (default)</span></span><br/> | <span data-ttu-id="d8425-120">Désactivé</span><span class="sxs-lookup"><span data-stu-id="d8425-120">Disabled</span></span><br/>                |
| <span data-ttu-id="d8425-121">Notransactions</span><span class="sxs-lookup"><span data-stu-id="d8425-121">NoTransactions</span></span><br/>           | <span data-ttu-id="d8425-122">Non pris en charge (par défaut)</span><span class="sxs-lookup"><span data-stu-id="d8425-122">Not Supported (default)</span></span><br/> |
| <span data-ttu-id="d8425-123">RequiresTransaction</span><span class="sxs-lookup"><span data-stu-id="d8425-123">RequiresTransaction</span></span> <br/>     | <span data-ttu-id="d8425-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d8425-124">Required</span></span><br/>                |
| <span data-ttu-id="d8425-125">UsesTransaction</span><span class="sxs-lookup"><span data-stu-id="d8425-125">UsesTransaction</span></span> <br/>         | <span data-ttu-id="d8425-126">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8425-126">Supported</span></span><br/>               |
| <span data-ttu-id="d8425-127">RequiresNewTransaction</span><span class="sxs-lookup"><span data-stu-id="d8425-127">RequiresNewTransaction</span></span> <br/>  | <span data-ttu-id="d8425-128">Nouveau requis</span><span class="sxs-lookup"><span data-stu-id="d8425-128">Requires New</span></span><br/>            |



 

<span data-ttu-id="d8425-129">Vous pouvez également accéder par programme à la propriété **MTSTransactionMode** à l’aide de l’API bibliothèque d’administration com+.</span><span class="sxs-lookup"><span data-stu-id="d8425-129">The **MTSTransactionMode** property can also be accessed programmatically by using the COM+ Administration Library API.</span></span>

 

 




