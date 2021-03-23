---
title: Historique des niveaux de fonctionnalité DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 92f5a004b73d608a3958ae0edfa8c6d6b6a523d6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548626"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="1f2b9-103">Historique des niveaux de fonctionnalité DirectML</span><span class="sxs-lookup"><span data-stu-id="1f2b9-103">DirectML feature level history</span></span>

<span data-ttu-id="1f2b9-104">Pour un historique général des versions de DirectML, consultez [l’historique des versions DirectML](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="1f2b9-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="1f2b9-105">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="1f2b9-105">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="1f2b9-106">Introduit dans DirectML version 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-106">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="1f2b9-107">Ajout de la prise en charge des opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-107">Added support for the following operators.</span></span>

* [<span data-ttu-id="1f2b9-108">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span><span class="sxs-lookup"><span data-stu-id="1f2b9-108">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="1f2b9-109">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-109">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="1f2b9-110">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-110">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="1f2b9-111">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-111">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="1f2b9-112">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-112">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="1f2b9-113">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-113">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="1f2b9-114">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-114">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="1f2b9-115">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-115">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="1f2b9-116">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-116">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="1f2b9-117">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-117">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="1f2b9-118">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-118">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="1f2b9-119">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-119">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="1f2b9-120">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-120">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="1f2b9-121">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-121">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="1f2b9-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="1f2b9-123">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-123">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="1f2b9-124">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-124">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="1f2b9-125">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-125">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="1f2b9-126">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-126">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="1f2b9-127">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-127">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="1f2b9-128">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f2b9-128">Added the following enhancements.</span></span>

* <span data-ttu-id="1f2b9-129">Le nombre maximal de dimensions de tenseur a été augmenté de 5 à 8.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-129">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="1f2b9-130">Consultez [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1f2b9-130">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="1f2b9-131">Une prise en charge supplémentaire des types de données entiers a été ajoutée aux opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-131">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="1f2b9-132">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-132">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="1f2b9-133">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-133">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="1f2b9-134">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** et **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-134">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="1f2b9-135">**DML_OPERATOR_REDUCE**, lors de l’utilisation de **DML_REDUCE_FUNCTION_ARGMIN** ou **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-135">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="1f2b9-136">Les types de données 64 bits suivants ont été ajoutés et sont pris en charge par les opérateurs Select.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-136">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="1f2b9-137">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-137">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="1f2b9-138">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-138">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="1f2b9-139">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-139">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="1f2b9-140">Fonctionnalités dépréciées.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-140">Deprecated functionality.</span></span>

* <span data-ttu-id="1f2b9-141">**DML_REDUCE_FUNCTION_ARGMAX** et **DML_REDUCE_FUNCTION_ARGMIN** ont été dépréciés.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-141">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="1f2b9-142">Il est préférable d’utiliser les opérateurs **DML_OPERATOR_ARGMIN** et **DML_OPERATOR_ARGMAX** autonomes à leur place.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-142">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="1f2b9-143">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="1f2b9-143">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="1f2b9-144">Introduit dans DirectML version 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-144">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="1f2b9-145">Ajout des API suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-145">Added the following APIs.</span></span>

* [<span data-ttu-id="1f2b9-146">Interface IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="1f2b9-146">IDMLDevice1 interface</span></span>](./directml/nn-directml-idmldevice1.md)
* <span data-ttu-id="1f2b9-147">Prise en charge des graphiques d’opérateur (consultez [IDMLDevice1 :: CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span><span class="sxs-lookup"><span data-stu-id="1f2b9-147">Operator graph support (see [IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span></span>

<span data-ttu-id="1f2b9-148">Ajout de la prise en charge des opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-148">Added support for the following operators.</span></span>

* <span data-ttu-id="1f2b9-149">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-149">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="1f2b9-150">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-150">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="1f2b9-151">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-151">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="1f2b9-152">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-152">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="1f2b9-153">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-153">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="1f2b9-154">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-154">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="1f2b9-155">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-155">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="1f2b9-156">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-156">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="1f2b9-157">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-157">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="1f2b9-158">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-158">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="1f2b9-159">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-159">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="1f2b9-160">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-160">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="1f2b9-161">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-161">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="1f2b9-162">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-162">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="1f2b9-163">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-163">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="1f2b9-164">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-164">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="1f2b9-165">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-165">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="1f2b9-166">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-166">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="1f2b9-167">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-167">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="1f2b9-168">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-168">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="1f2b9-169">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-169">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="1f2b9-170">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-170">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="1f2b9-171">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-171">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="1f2b9-172">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-172">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="1f2b9-173">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f2b9-173">Added the following enhancements.</span></span>

* <span data-ttu-id="1f2b9-174">Une prise en charge supplémentaire des types de données entiers a été ajoutée aux opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-174">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="1f2b9-175">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-175">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="1f2b9-176">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-176">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="1f2b9-177">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-177">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="1f2b9-178">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-178">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="1f2b9-179">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-179">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="1f2b9-180">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-180">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="1f2b9-181">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-181">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="1f2b9-182">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-182">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="1f2b9-183">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-183">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="1f2b9-184">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-184">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="1f2b9-185">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-185">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="1f2b9-186">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-186">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="1f2b9-187">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-187">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="1f2b9-188">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-188">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="1f2b9-189">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-189">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="1f2b9-190">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-190">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="1f2b9-191">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-191">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="1f2b9-192">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-192">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="1f2b9-193">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-193">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="1f2b9-194">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-194">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="1f2b9-195">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-195">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="1f2b9-196">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-196">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="1f2b9-197">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-197">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="1f2b9-198">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-198">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="1f2b9-199">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-199">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="1f2b9-200">**DML_OPERATOR_TOP_K** et **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-200">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="1f2b9-201">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-201">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="1f2b9-202">**DML_OPERATOR_REDUCE**, lors de l’utilisation de l’une des fonctions de réduction suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-202">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="1f2b9-203">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-203">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="1f2b9-204">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-204">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="1f2b9-205">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-205">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="1f2b9-206">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-206">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="1f2b9-207">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-207">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="1f2b9-208">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-208">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="1f2b9-209">Restrictions de forme de tenseur souple pour **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-209">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="1f2b9-210">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="1f2b9-210">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="1f2b9-211">Introduit dans DirectML version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-211">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="1f2b9-212">Ajout des API suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-212">Added the following APIs.</span></span>
* [<span data-ttu-id="1f2b9-213">Fonction DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="1f2b9-213">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="1f2b9-214">Énumération DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="1f2b9-214">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="1f2b9-215">Requêtes au niveau des fonctionnalités (voir [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="1f2b9-215">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="1f2b9-216">Ajout de la prise en charge des opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-216">Added support for the following operators.</span></span>

* <span data-ttu-id="1f2b9-217">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-217">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="1f2b9-218">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-218">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="1f2b9-219">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-219">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="1f2b9-220">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-220">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="1f2b9-221">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-221">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="1f2b9-222">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-222">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="1f2b9-223">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-223">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="1f2b9-224">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-224">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="1f2b9-225">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-225">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="1f2b9-226">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-226">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="1f2b9-227">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-227">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="1f2b9-228">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-228">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="1f2b9-229">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-229">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="1f2b9-230">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-230">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="1f2b9-231">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-231">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="1f2b9-232">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-232">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="1f2b9-233">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-233">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="1f2b9-234">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-234">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="1f2b9-235">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-235">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="1f2b9-236">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f2b9-236">Added the following enhancements.</span></span>

* <span data-ttu-id="1f2b9-237">Lors de la liaison d’une ressource d’entrée pour la distribution d’un [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), il est maintenant légal de fournir une ressource avec [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (en plus de **D3D12_HEAP_TYPE_DEFAULT**), à condition que les propriétés de tas appropriées soient également définies.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-237">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="1f2b9-238">Consultez [liaison dans DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="1f2b9-238">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="1f2b9-239">Les opérateurs booléens logiques suivants prennent désormais en charge les dizaines de temps de sortie **UINT8** , en plus de la prise en charge existante de **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-239">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="1f2b9-240">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-240">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="1f2b9-241">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-241">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="1f2b9-242">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-242">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="1f2b9-243">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-243">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="1f2b9-244">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-244">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="1f2b9-245">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-245">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="1f2b9-246">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-246">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="1f2b9-247">5J les fonctions d’activation prennent désormais en charge l’utilisation de Strides sur leurs dizaines d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-247">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="1f2b9-248">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="1f2b9-248">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="1f2b9-249">Niveau de fonctionnalité dans lequel DirectML a été introduit.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-249">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f2b9-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f2b9-250">See also</span></span>

<span data-ttu-id="1f2b9-251">[Historique des](./dml-version-history.md) 
 versions de DirectML [Énumération DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) 
 [DMLCreateDevice1 fonction](./directml/nf-directml-dmlcreatedevice1.md) 
 ) [Structure DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)</span><span class="sxs-lookup"><span data-stu-id="1f2b9-251">[DirectML version history](./dml-version-history.md)
[DML_FEATURE_LEVEL enumeration](/windows/win32/api/directml/ne-directml-dml_feature_level)
[DMLCreateDevice1 function](./directml/nf-directml-dmlcreatedevice1.md)
[DML_FEATURE_QUERY_FEATURE_LEVELS structure](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)</span></span>