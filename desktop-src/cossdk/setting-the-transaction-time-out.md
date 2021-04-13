---
description: Vous pouvez définir manuellement le délai d’expiration pour les transactions à l’aide de l’outil d’administration Services de composants, ou vous pouvez configurer par programme le délai d’expiration à l’aide des interfaces d’administration COM+.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Définition de la Time-Out de transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483784"
---
# <a name="setting-the-transaction-time-out"></a><span data-ttu-id="ccf2b-103">Définition de la Time-Out de transaction</span><span class="sxs-lookup"><span data-stu-id="ccf2b-103">Setting the Transaction Time-Out</span></span>

<span data-ttu-id="ccf2b-104">Vous pouvez définir manuellement le délai d’expiration pour les transactions à l’aide de l’outil d’administration Services de composants, ou vous pouvez configurer par programme le délai d’expiration à l’aide des [interfaces d’administration com+](com--administration-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="ccf2b-104">You can manually set the time-out for transactions by using the Component Services administrative tool, or you can programmatically configure the time-out by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span> <span data-ttu-id="ccf2b-105">Le délai d’attente peut être configuré au niveau de l’ordinateur local et également pour les composants individuels.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-105">The time-out can be configured at the local computer level and also for individual components.</span></span>

<span data-ttu-id="ccf2b-106">**Pour définir le délai d’expiration de la transaction pour l’ordinateur local à l’aide de l’outil d’administration Services de composants**</span><span class="sxs-lookup"><span data-stu-id="ccf2b-106">**To set the transaction time-out for the local computer by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="ccf2b-107">Dans l’arborescence de la console, cliquez avec le bouton droit sur l’ordinateur local que vous souhaitez configurer, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-107">In the console tree, right-click the local computer you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="ccf2b-108">Dans la boîte de dialogue Propriétés de l’ordinateur, cliquez sur l’onglet **options** .</span><span class="sxs-lookup"><span data-stu-id="ccf2b-108">In the computer properties dialog box, click the **Options** tab.</span></span>

3.  <span data-ttu-id="ccf2b-109">Sous **délai d’expiration** de la transaction, entrez le délai d’expiration de la transaction en secondes.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-109">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="ccf2b-110">Le délai d’attente par défaut est de 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-110">The default time-out is 60 seconds.</span></span>

4.  <span data-ttu-id="ccf2b-111">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-111">Click **OK**.</span></span>

<span data-ttu-id="ccf2b-112">**Pour définir le délai d’expiration de la transaction pour un composant à l’aide de l’outil d’administration Services de composants**</span><span class="sxs-lookup"><span data-stu-id="ccf2b-112">**To set the transaction time-out for a component by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="ccf2b-113">Dans l’arborescence de la console, cliquez avec le bouton droit sur le composant que vous souhaitez configurer, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-113">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="ccf2b-114">Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **transactions** .</span><span class="sxs-lookup"><span data-stu-id="ccf2b-114">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="ccf2b-115">Activez la case à cocher **remplacer la valeur du délai d’expiration de la transaction globale**.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-115">Check the box labeled **Override global transaction timeout value**.</span></span>

    > [!Note]  
    > <span data-ttu-id="ccf2b-116">Vous ne pouvez pas activer la case à cocher pour remplacer la valeur du délai d’attente de la transaction globale si la **prise en charge** de la transaction est définie sur **désactivé**, **non pris en charge** ou **pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-116">You cannot check the box to override the global transaction time-out value if the **Transaction support** is set to **Disabled**, **Not Supported**, or **Supported**.</span></span>

     

4.  <span data-ttu-id="ccf2b-117">Sous **délai d’expiration** de la transaction, entrez le délai d’expiration de la transaction en secondes.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-117">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="ccf2b-118">Le délai d’attente par défaut est de 0 seconde, ce qui signifie que le composant ne provoquera jamais l’expiration du délai d’attente de la transaction.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-118">The default time-out is 0 seconds, which means that the component will never cause the transaction to time out.</span></span>

5.  <span data-ttu-id="ccf2b-119">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccf2b-119">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccf2b-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ccf2b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccf2b-121">Gestion des transactions automatiques dans COM+</span><span class="sxs-lookup"><span data-stu-id="ccf2b-121">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



