---
title: Services en mémoire tampon
description: Services en mémoire tampon
ms.assetid: 4816ab05-42fc-4c22-b753-8fd153d88c27
keywords:
- e/s de fichier multimédia, services mis en mémoire tampon
- e/s de fichier, services mis en mémoire tampon
- entrées et sorties (e/s), services mis en mémoire tampon
- E/s (entrée et sortie), services mis en mémoire tampon
- e/s mises en mémoire tampon
- mmioOpen fonction)
- mémoire tampon d’e/s interne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d014ed765609dd43886cc7b33987f8fd5ac7e65a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007222"
---
# <a name="buffered-services"></a>Services en mémoire tampon

La majeure partie de la surcharge des e/s de fichier se produit lors de l’accès à l’appareil multimédia. Si vous lisez ou écrivez de nombreux petits blocs d’informations, l’appareil peut passer beaucoup de temps à se déplacer vers l’emplacement physique sur le support pour chaque opération de lecture ou d’écriture. Dans ce cas, vous pouvez obtenir de meilleures performances en utilisant les services d’e/s de fichier mis en mémoire tampon. Avec les e/s mises en mémoire tampon, le gestionnaire d’e/s de fichier gère une mémoire tampon intermédiaire plus grande que les blocs d’informations que vous lisez ou écrivez. Elle accède à l’appareil uniquement lorsque la mémoire tampon doit être remplie ou écrite sur le disque.

Avant de configurer et d’utiliser des e/s de fichier mises en mémoire tampon, vous devez décider si vous souhaitez que le gestionnaire d’e/s de fichier ou l’application alloue la mémoire tampon. Il est plus simple de laisser le gestionnaire d’e/s de fichier allouer la mémoire tampon. Toutefois, vous pouvez laisser l’application allouer la mémoire tampon si vous souhaitez accéder directement à la mémoire tampon ou ouvrir un fichier de mémoire. Pour plus d’informations sur l’utilisation des fichiers de mémoire, consultez [exécution d’e/s de fichier mémoire](performing-memory-file-i-o.md). Pour obtenir un exemple d’accès direct à une mémoire tampon d’e/s, consultez [accès à un tampon d’e/s de fichier](accessing-a-file-i-o-buffer.md)

Une mémoire tampon allouée par le gestionnaire d’e/s de fichier est appelée une mémoire tampon d’e/s interne. Pour ouvrir un fichier pour les e/s mises en mémoire tampon à l’aide d’une mémoire tampon interne, spécifiez l' \_ indicateur MMIO ALLOCBUF quand vous ouvrez le fichier avec la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . L’illustration suivante montre l’état initial du tampon d’e/s de fichier une fois qu’un fichier a été ouvert pour une opération de lecture mise en mémoire tampon. La mise en mémoire tampon est transparente : vous lisez et recherchez comme si vous utilisiez des e/s non mises en mémoire tampon. La fonction **mmioOpen** a défini PchNext et *pchEndRead* pour qu’elle pointe vers le début de la mémoire tampon d’e/s de fichier.

![Capture d’écran montrant « pchEndRead » et « pchNext » pointant vers le début de la mémoire tampon d’e/s de fichier.](images/mmio7.gif)

L’illustration suivante montre l’état initial du tampon d’e/s de fichier une fois qu’un fichier a été ouvert pour une opération d’écriture en mémoire tampon. La fonction **mmioOpen** a défini **pchNext** pour pointer vers le début de la mémoire tampon d’e/s de fichier et **pchEndWrite** pour pointer vers la fin de la mémoire tampon.

![Capture d’écran montrant « pchNext » au début de la mémoire tampon d’e/s de fichier et « pchEndWrite » à la fin.](images/mmio11.gif)

La taille par défaut de la mémoire tampon d’e/s interne est de 8 Ko. Si cette taille n’est pas appropriée, vous pouvez utiliser la fonction [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) pour modifier la taille de la mémoire tampon. Vous pouvez également utiliser cette fonction pour activer la mise en mémoire tampon sur un fichier ouvert pour des e/s non mises en mémoire tampon, ou pour fournir votre propre mémoire tampon à utiliser comme fichier de mémoire.

Vous pouvez forcer l’écriture du contenu d’une mémoire tampon d’e/s sur le disque à l’aide de la fonction [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush) . Toutefois, lorsque vous fermez un fichier à l’aide de la fonction [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) , il n’est pas nécessaire d’appeler **mmioFlush** pour vider une mémoire tampon d’e/s ; la fonction **mmioClose** la vide automatiquement. Si l’espace disque est insuffisant, **mmioFlush** peut échouer, même si les appels précédents à la fonction [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) ont réussi. De même, **mmioClose** peut échouer lorsqu’il vide son tampon d’e/s.

Les applications qui sont sensibles aux performances, telles que celles qui diffusent des données en temps réel à partir d’un CD-ROM, peuvent optimiser les performances d’e/s de fichier en accédant directement à la mémoire tampon d’e/s. Vous devez faire attention si vous choisissez de le faire, car vous ignorez certaines des protections et la vérification des erreurs fournies par le gestionnaire d’e/s de fichier.

Le gestionnaire d’e/s de fichier multimédia utilise la structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) pour conserver les informations d’État relatives à un fichier ouvert. Vous utilisez trois membres dans cette structure pour lire et écrire le tampon d’e/s : **pchNext**, **pchEndRead** et **pchEndWrite**. Le membre **pchNext** pointe vers l’emplacement suivant dans la mémoire tampon pour la lecture ou l’écriture. Vous devez incrémenter ce membre lors de la lecture et de l’écriture de la mémoire tampon. Le membre **pchEndRead** identifie le dernier caractère valide que vous pouvez lire à partir de la mémoire tampon. De même, ce membre identifie le dernier emplacement dans la mémoire tampon que vous pouvez écrire. Plus précisément, **pchEndRead** et **pchEndWrite** pointent vers l’emplacement de mémoire qui suit les dernières données valides dans la mémoire tampon. Utilisez les fonctions [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) et [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) pour récupérer et définir des informations d’État sur le tampon d’e/s de fichier. L’illustration suivante montre l’état de la mémoire tampon d’e/s après que l’application a appelé **mmioAdvance** au cours d’une opération de lecture. La fonction **mmioAdvance** remplit la mémoire tampon et définit le pointeur **pchEndRead** à la fin de la mémoire tampon.

![Capture d’écran montrant « pchNext » au début de la mémoire tampon d’e/s de fichier et « pchEndRead » à la fin.](images/mmio8.gif)

Dans l’illustration suivante, l’application lit le tampon d’e/s à l’emplacement spécifié par **pchNext** et avance le pointeur.

![Capture d’écran qui affiche « pchNext » au milieu de la mémoire tampon d’e/s de fichier et « pchEndRead » à la fin.](images/mmio9.gif)

De même, pour une opération d’écriture, l’application écrit dans la mémoire tampon d’e/s et avance le pointeur **pchNext** , comme indiqué dans l’illustration suivante.

![Capture d’écran qui affiche « pchNext » au milieu de la mémoire tampon d’e/s de fichier et « pchEndWrite » à la fin.](images/mmio12.gif)

Une fois que l’application a rempli la mémoire tampon, elle appelle **mmioAdvance** pour vider la mémoire tampon sur le disque. La fonction **mmioAdvance** réinitialise **pchNext** pour qu’elle pointe vers le début de la mémoire tampon, comme indiqué dans l’illustration suivante.

![Capture d’écran qui affiche « pchNext » au début de la mémoire tampon d’e/s de fichier, la mémoire tampon au milieu de l’E O F et « pchEndWrite » à la fin de la mémoire tampon.](images/mmio13.gif)

Lorsque vous atteignez la fin de la mémoire tampon d’e/s, vous devez avancer le tampon pour le remplir à partir du disque, si vous lisez ou le videz sur le disque, si vous écrivez. Utilisez la fonction [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance) pour avancer un tampon d’e/s. Pour remplir une mémoire tampon d’e/s à partir du disque, utilisez **mmioAdvance** avec l' \_ indicateur de lecture MMIO. Si les données restantes dans le fichier ne sont pas suffisantes pour remplir la mémoire tampon, le membre **pchEndRead** de la structure **MMIOINFO** pointe vers l’emplacement qui suit le dernier octet valide dans la mémoire tampon. Pour vider un tampon sur un disque, définissez l' \_ indicateur de modification MMIO dans le membre **dwFlags** de la structure **MMIOINFO** , puis appelez **MMIOADVANCE** avec l’indicateur d' \_ écriture MMIO.

Par exemple, lors d’une opération de lecture, la fonction **mmioAdvance** définit **pchEndRead** pour qu’elle pointe vers la fin des données valides dans la mémoire tampon, comme indiqué dans l’illustration suivante.

![Capture d’écran qui affiche « pchNext » au début de la mémoire tampon d’e/s de fichier, la mémoire tampon à la fin de E O F et « pchEndRead » à la fin de la mémoire tampon.](images/mmio10.gif)

De même, au cours d’une opération d’écriture, l’application appelle **mmioAdvance** pour vider la mémoire tampon et avancer **pchNext** à la fin des données valides dans la mémoire tampon, comme indiqué dans l’illustration suivante.

![image de tampon d’e/s de fichier](images/mmio14.gif)

 

 